<template>
    <div class="card">
    <v-card
            hover="true , 4dp"

            max-width="400"
    >
        <v-img
                class="black--text align-end"
                height="200px"
                :src="image"
        >


        </v-img>
        <v-card-title>{{title | uppercase }}</v-card-title>
        <v-card-subtitle class="pb-0">{{price}}</v-card-subtitle>

        <v-card-text class="text--primary">
            <div v-for="(description, index) in descriptions" :key="index">{{description}}</div>


        </v-card-text>

    </v-card>
    </div>
</template>

<script>
    export default {
        name: 'card',
        props:{
            image: String,
            title: String,
            price: String,
            descriptions: Array,
            index: Number,


        },
        filters: {
            uppercase: function (value) {

                return value.toUpperCase()
            }
        },



    }

</script>

<style scoped>

</style>