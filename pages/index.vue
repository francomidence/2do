<template>
  <v-layout column justify-center align-center>
    <v-flex xs12 sm8 md6>
      <div class="text-center"></div>
      <v-card>
        <v-card-title class="headline"></v-card-title>
        <v-card-text>
          <p class="display-2" style="font-weight: bold">
            Encuentra un hobby en 5 clicks.
          </p>
        </v-card-text>
        <v-card-actions>
          <v-spacer />
        </v-card-actions>
      </v-card>
      <carousel />
      <home-card />
    </v-flex>
  </v-layout>
</template>

<script>
import Carousel from '@/components/Carousel.vue'
import HomeCard from '@/components/HomeCard.vue'

export default {
  components: {
    Carousel,
    HomeCard
  }
}
</script>
