<template>
  <v-card img="/img/index_img_1.jpg" 
            height="200px"
            :to="routerTo" class="d-flex justify-center">
    <v-card-title class="grey--text text--darken-3"> {{title}} </v-card-title>
  </v-card>
</template>

<script>
export default {
    props : {
        title: String,
        imgUrl: String,
        routerTo: String
    }
};
</script>

<style>
</style>