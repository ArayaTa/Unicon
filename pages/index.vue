<template>
  <v-row justify="center" align="center" style="">
    <v-col cols="12" sm="8" md="6">
      <div class="text-center">
        <logo />
        <vuetify-logo />
      </div>
      <v-card
        style="
          background-image: url(https://images.fineartamerica.com/images/artworkimages/mediumlarge/2/cute-unicorn-beautiful-magical-horse-jonathan-golding.jpg);
        "
      >
        <!-- <v-card-title class="headline"> 🌈🌈🌈🌈🌈🌈🌈🌈🌈🌈🌈🌈 </v-card-title>-->
        <v-card-text>
          <p>🦄 𝓓𝓸𝓷'𝓽 𝓯𝓸𝓰𝓮𝓽 𝓯𝓸𝓵𝓵𝓸𝔀 𝓶𝓮 🦄</p>
          <p>
            𝒲𝑒𝓁𝒸𝑜𝓂𝑒 𝓉𝑜 𝓌𝑒𝒷𝓈𝒾𝓉𝑒 𝓎𝑜𝓊 𝒸𝒶𝓃 𝓈𝑒𝒶𝓇𝒸𝒽 𝒶𝓁𝓁 𝓉𝒽𝑒 𝒢𝐼𝐹𝓈 𝒶𝓃𝒹 𝒮𝓉𝒾𝒸𝓀𝑒𝓇𝓈 𝑜𝓉𝒽𝑒𝓇.
            <a
              href="https://giphy.com/"
              target="_blank"
              rel="noopener noreferrer"
            >
              𝓖𝓘𝓟𝓗𝓨 </a
            >.
          </p>
        </v-card-text>
        <v-card-actions>
          <v-spacer />
          <v-btn color="pink accent-1 " nuxt to="/inspire"
            >🍦𝓛𝓮𝓽 𝓲𝓼 𝓰𝓸🍦
          </v-btn>
          <v-btn color="pink lighten-4" class="Profile" nuxt to="/Profile"
            >🌈
          </v-btn>
        </v-card-actions>
      </v-card>
    </v-col>
  </v-row>
</template>

<script>
import Logo from '~/components/img/unicon.gif'
import VuetifyLogo from '~/components/VuetifyLogo.vue'

export default {
  components: {
    Logo,
    VuetifyLogo,
  },
}
</script>
