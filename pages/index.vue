<template>
  <div>
    <AppSlider />
    <galleryGrid />
  </div>
</template>

<script>
import galleryGrid from '@/components/galleryGrid.vue'
import AppSlider from '@/components/AppSlider.vue'
export default {
  components : {
    galleryGrid,
    AppSlider
    }
}
</script>