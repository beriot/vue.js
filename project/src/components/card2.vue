<template>
    <v-card   class="mx-auto" max-width="500"   hover="true , 4dp">

        <v-container fluid>
            <v-row dense>
                <v-col  v-for="card in cards" :key="card.title" :cols="card.flex">
                    <v-card>
                        <v-img
                                :src="card.src"
                                class="white--text align-end"
                                gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.5)"
                                height="200px"
                        >
                            <v-card-title v-text="card.title"></v-card-title>
                        </v-img>


                    </v-card>
                </v-col>
            </v-row>
        </v-container>
    </v-card>
</template>

<script>
    export default {
        name: "card2",
        data: () => ({
            cards: [
                { title: 'T120', src: 'https://images.triumphmotorcycles.co.uk/media-library/images/motorcycles/modern-classics/t120%20new/jet-black-rhs-1920x1080.png', flex: 12 },
                { title: 'ROCKET 3 R', src: 'https://images.triumphmotorcycles.co.uk/media-library/images/configurator/optimised-baselayers/my20-rocket-3-rhs-red-opt.png', flex: 6 },
                { title: 'TIGER 1200 XR', src: 'https://images.triumphmotorcycles.co.uk/media-library/images/motorcycles/adventure-touring/base%20layers/vg3-rhs-jet-black1920x1080.png', flex: 6 },
            ],
        }),
    }
</script>

<style scoped>

</style>