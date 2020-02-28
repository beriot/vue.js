    <template>

            <v-carousel height="650px"  >
                <v-carousel-item
                        v-for="(item,i) in items"
                        :key="i"
                        :src="item.src"
                        reverse-transition="fade-transition"
                        transition="fade-transition"
                ></v-carousel-item>
            </v-carousel>

    </template>




    <script>
        export default {
            name: "Carousel",

                data () {

                    return {
                        items: [
                            {
                                src: 'https://images.triumphmotorcycles.co.uk/media-library/images/motorcycles/roadsters-supersports/street%20triple%202020/street%20triple%20rs%202020/street-triple-rs-20my-main-page-hero-1920x1080px.jpg',
                            },
                            {
                                src: 'https://acidmoto.ch/cms/sites/default/files/new_street_triple_rs_-_dynamic_9.jpg',
                            },
                            {
                                src: 'https://www.actumoto.ch/wp-content/uploads/2019/10/Triumph_Street_Triple_RS_020small_Launch_4200.jpg',
                            },
                            {
                                src: 'https://acidmoto.ch/cms/sites/default/files/img/epsilon/t/triumph_speed_triple_1050_s_2018-6.jpg',
                            },
                        ],
                    }
                },
            }
    </script>

<style scoped>



</style>