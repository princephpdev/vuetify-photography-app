<template>
  <v-carousel cycle show-arrows-on-hover hide-delimiter-background>
    <v-carousel-item
      v-for="(item,i) in items"
      :key="i"
      :src="item.src"
    >
        <v-row
          class="fill-height"
          align="center"
          justify="center"
        >
          <div class="display-1 white--text hidden-sm-and-down">{{ item.src }}</div>
        </v-row>
    </v-carousel-item>
  </v-carousel>
</template>

<script>
export default {
    data () {
      return {
        items: [
          {
            src: 'https://cdn.vuetifyjs.com/images/carousel/squirrel.jpg',
          },
          {
            src: 'https://cdn.vuetifyjs.com/images/carousel/sky.jpg',
          },
          {
            src: 'https://cdn.vuetifyjs.com/images/carousel/bird.jpg',
          },
          {
            src: 'https://cdn.vuetifyjs.com/images/carousel/planet.jpg',
          },
        ],
      }
    },
  }
</script>