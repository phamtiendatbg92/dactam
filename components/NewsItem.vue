<template>
  <v-card hover height="100%">
    <v-img src="/img/index_img_1.jpg"> </v-img>
    <v-card-title> Title </v-card-title>
    <v-card-subtitle>
      <v-icon>mdi-calendar-month</v-icon> date time
    </v-card-subtitle>
    <v-card-text class="d-block text-truncate"> {{name}} </v-card-text>
    <v-card-actions>
      <v-btn>Xem thêm</v-btn>
    </v-card-actions>
  </v-card>
</template>

<script>
export default {
  data() {
    return {
        name : "",
    };
  },
  async created() {
     const result = await this.$axios.$get("test");
     this.name = result[0].name;
  },
};
</script>

<style>
</style>