<template>
  <div>
    <v-app id="inspire">
      <v-carousel
        cycle
        height="400"
        hide-delimiter-background
        show-arrows-on-hover
      >
        <v-carousel-item v-for="(slide, i) in slides" :key="i" :src="slide.src">
          <v-parallax :src="slide.src">
            <v-row class="fill-height" align="center" justify="center"></v-row>
          </v-parallax>
        </v-carousel-item>
      </v-carousel>
    </v-app>
  </div>
</template>

<script>
export default {
  data() {
    return {
      colors: [
        'indigo',
        'warning',
        'pink darken-2',
        'red lighten-1',
        'deep-purple accent-4'
      ],
      slides: [
        {
          titulo: 'Deporte',
          src: require('@/assets/deportebg.jpg')
        },
        {
          titulo: 'Musica',
          src: require('@/assets/musica.jpg')
        },
        {
          titulo: 'Baile',
          src: require('@/assets/baile.jpg')
        },
        {
          titulo: 'Arte',
          src: require('@/assets/arte.jpeg')
        },
        {
          titulo: 'Idioma',
          src: require('@/assets/idioma.jpg')
        }
      ]
    }
  }
}
</script>

<style lang="scss" scoped></style>
