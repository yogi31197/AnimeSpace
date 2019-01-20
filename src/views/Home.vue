<template>
  <div>
    <v-layout row warp>
      <v-flex xs12 sm6 md4 lg3 v-for="show in shows" :key="show.id">
        <v-card>hello</v-card>
      </v-flex>
    </v-layout>
  </div>
</template>

<script>
export default {
  components: {
    data() {
      return {
        shows: [
          {
            id: "1",
            title: "That time i got reincarnatied as a slime",
            ctg: "Fantasy,Advanture,Action",
            status: "Ongoing"
          },
          {
            id: "2",
            title: "Fairy tail",
            ctg: "Fantasy,Advanture,Action",
            status: "Ongoing"
          },
          {
            id: "3",
            title: "Death note",
            ctg: "Mystery,Thriller,Suspense",
            status: "Completed"
          }
        ]
      };
    }
  }
};
</script>

<style>
</style>
