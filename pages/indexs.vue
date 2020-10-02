<template>
  <div class="container">
    <v-col justify="center" align="center">
      <v-col cols="6" sm="4" md="5">
        <v-img
          src="https://media0.giphy.com/media/kZuruX5l9fhxQms7Co/source.gif"
          max-width="230"
        />
        <p><br /></p>
      </v-col>
      <v-text-field
        v-model="keyword"
        size="lg"
        type="text"
        placeholder="𝒮𝐸𝒜𝑅𝒞𝐻 𝒩♡𝒲  🔥"
        solo
        background-color="teal lighten-4"
      ></v-text-field>
      <p><br /></p>
      <v-btn color="#B39DDB" @click="searchData()">𝒮𝐸𝒜𝑅𝒞𝐻 𝒢𝐼𝐹 𝐻𝐸𝑅𝐸 </v-btn>
      <p><br /></p>
    </v-col>
    <div class="text-center card overflow-hidden row no-gutters">
      <v-card
        v-for="data in resultData"
        :key="data.id"
        color="#FCE4EC"
        class="mb-5 ml-5"
        max-width="350"
      >
        <v-card-text
          :key="data.id"
          justify="center"
          class="headline font-weight-bold"
          >{{ data.import_datetime }}</v-card-text
        >
        <video
          :key="data.id"
          class="rounded"
          type="video"
          :src="data.images.original.mp4"
          autoplay=""
          loop=""
          style="max-width: 100%"
        ></video>
        <v-btn
          color="#BCAAA4"
          nuxt
          :to="{
            name: 'detail-id',
            params: {
              id: data.id,
              title: data.title,
              import_datetime: data.import_datetime,
              type: data.type,
              video: data.images.original.mp4,
              username: data.username,
              url: data.url,
            },
          }"
          >👉𝓖𝓞 𝓣𝓞 𝓛𝓘𝓝𝓚👈</v-btn
        >
        <p><br /></p>
      </v-card>
    </div>
  </div>
</template>
<script>
import axios from 'axios'
export default {
  data() {
    return {
      resultData: null,
      keyword: '',
    }
  },
  methods: {
    searchData() {
      axios
        .get(
          'https://api.giphy.com/v1/gifs/search?api_key=39vI8skUqOzHnLMOJZiRkLKJ7SIWbQ4J&q=' +
            this.keyword +
            '&limit=30'
        )
        .then((response) => {
          this.resultData = response.data.data
        })
        .catch((err) => {
          // eslint-disable-next-line no-console
          console.log(err)
        })
    },
  },
}
</script>
<style>
#app {
  background-image: url(https://i.pinimg.com/originals/35/f2/a5/35f2a54da02f0cefb0bc6e13b6c8f310.jpg);
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  margin-top: 60px;
}
</style>
