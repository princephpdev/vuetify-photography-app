<template>
<v-app>
  <topmenu />
    <nuxt />
  <AppFooter />
</v-app>
</template>

<script>
import topmenu from '@/components/nav/topmenu.vue'
import AppFooter from '@/components/AppFooter.vue'
export default {
  components : {
    topmenu,
    AppFooter
  }
}
</script>