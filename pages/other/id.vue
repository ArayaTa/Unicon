<template>
  <div class="text-center card overflow-hidden">
    <v-col justify="center" align="center">
      <v-card color="" class="mb-6 ml-6" max-width="350">
        <video
          class="rounded"
          type="video"
          :src="gif.video"
          autoplay=""
          loop=""
          style="max-width: 100%"
        ></video>
        <h2>𝗗𝗲𝘁𝗮𝗶𝗹</h2>
        <h3>𝗜𝗗 : {{ gif.id }}</h3>
        <h3>𝗧𝗶𝘁𝗹𝗲 : {{ gif.title }}</h3>
        <h3>𝗧𝘆𝗽𝗲 : {{ gif.type }}</h3>
        <h3>𝗨𝘀𝗲𝗿𝗻𝗮𝗺𝗲 : {{ gif.username }}</h3>
        <h3>𝗗𝗮𝘁𝗮 : {{ gif.import_datetime }}</h3>
        <p><br /></p>
        <v-btn color="#E6EE9C" :href="gif.url">👉𝓖𝓞 𝓣𝓞 𝓛𝓘𝓝𝓚👈</v-btn>
        <p><br /></p>
      </v-card>
    </v-col>
  </div>
</template>
<script>
export default {
  data() {
    return {
      gif: this.$route.params,
    }
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
