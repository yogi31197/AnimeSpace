<template>
  <div>
    <v-layout row warp>
      <v-flex xs12 sm6 md4 lg4 v-for="show in shows" :key="show.id">
        <v-tooltip top color="purple">
        <v-card class="ma-2" slot="activator">
          <v-responsive :class="`${show.status} ${show.type}`">
            <v-img :src="show.img" alt="Image" height="200px"/>
          </v-responsive>
          <v-layout row class="ml-0">
            <v-flex xs8>
              <v-card-text class="subheading font-weight-bold mb-0 pb-0">{{show.title}}</v-card-text>
              <v-card-text class="red--text pt-0">{{show.ctg}}</v-card-text>
            </v-flex>
            <v-flex>
              <div style="float:right">
                <v-chip class="mt-4 mr-5 pr-0 primary white--text">{{show.episode}}</v-chip>
              </div>
            </v-flex>
          </v-layout>
        </v-card>
        <span>{{show.title}} | {{show.type}} | Episode :{{show.episode}} | {{show.status}}</span>
        </v-tooltip>
      </v-flex>
    </v-layout>
  </div>
</template>

<script>
export default {
  components: {},
  data() {
    return {
      shows: [
        {
          id: "1",
          title: "That time i got reincarnatied as a slime",
          ctg: "Fantasy,Advanture,Action",
          status: "Ongoing",
          img: "https://cdn.myanimelist.net/images/anime/1353/97915l.jpg",
          episode: "10",
          type:"Subbed"
        },
        {
          id: "2",
          title: "Fairy tail",
          ctg: "Fantasy,Advanture,Action",
          status: "Ongoing",
          img: "https://cdn.myanimelist.net/images/anime/1536/93863l.jpg",
          episode: "8",
          type:"Dubbed"
        },
        {
          id: "3",
          title: "Death note",
          ctg: "Mystery,Thriller,Suspense",
          status: "Completed",
          img: "https://cdn.myanimelist.net/images/anime/9/21498.jpg",
          episode: "15",
          type:"Subbed"
        }
      ]
    };
  }
};
</script>

<style>
.Ongoing{
  border-right: 4px solid  slateblue
}
.Subbed{
  border-left: 4px tomato solid
}
</style>
