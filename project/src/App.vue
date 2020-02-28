<template>
  <v-app>


    <v-content>
        <Nav></Nav>
      <Carousel></Carousel>
        <div style="background-color: #FFFAF4; padding-bottom: 40px">
      <moto></moto>
        </div>

      <!--<HelloWorld/>-->
      <div style="display: flex; justify-content: space-around; background-color: #DADBDD; padding-top: 40px; padding-bottom: 20px">
     <card v-for="(content, index) in contents" :title="content.title" :price="content.price" :key="index" :descriptions="content.descriptions" :index="index" :image="content.image" ></card>
      </div>

        <div style="display: flex; justify-content: space-around; background-color: #DADBDD; padding-top: 20px; padding-bottom: 20px" >
            <card2></card2>
        </div>

    </v-content>
  </v-app>
</template>

<script>
//import HelloWorld from './components/HelloWorld';
import Nav from './components/Nav';
import Carousel from "./components/Carousel";
import Moto from "./components/moto";
import Card from "./components/card";

import Card2 from "./components/card2";
export default {
  name: 'App',

  components: {
   Card,
    Moto,
    Carousel,
    // HelloWorld,
    Nav,
      Card2,
  },

  data() {
    return {
      contents: [
        {
         image: "https://images.triumphmotorcycles.co.uk/media-library/images/motorcycles/modern-classics/t120%20new/jet-black-rhs-1920x1080.png",
          title: "t120",
          price: "12 800.00 €",
          descriptions: [
            "La Bonneville originelle de 1959 est incontestablement",
            "une icône du monde motocycliste.",
            " Adulée dans le monde entier par toutes les générations",
            "et tous les styles de pilotes,",
             "elle incarne pour beaucoup l’essence même de la moto."
          ],



        },
        {
            image: "https://images.triumphmotorcycles.co.uk/media-library/images/configurator/optimised-baselayers/my20-rocket-3-rhs-red-opt.png",
          title: "rocket 3 r",
          price: "22 400,00 €",
          descriptions: [
            "C’est la genèse de la toute nouvelle génération d’une légende Triumph. Équipée d’un moteur de 2500 cm3, soit la plus grosse cylindrée du monde pour une moto de série, la nouvelle gamme Rocket 3 produit un couple imbattable et une accélération inégalée, en plus d’une expérience de conduite incroyablement inoubliable, dynamique et raffinée."


          ],

        },
        {
            image: "https://images.triumphmotorcycles.co.uk/media-library/images/motorcycles/adventure-touring/base%20layers/vg3-rhs-jet-black1920x1080.png",
          title: "tiger 1200 xr",
          price: "16 100,00 €",
          descriptions: [
            "Notre meilleure gamme Adventure a évolué. Désormais plus légères et plus agiles, avec 100 améliorations dont une importante mise à jour de leur moteur pour une puissance plus immédiate, ces motos sont faites pour des aventures épiques.",

          ],

        }
      ],

    }
  }
}
</script>
