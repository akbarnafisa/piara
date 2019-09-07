<template>
  <div>
    <the-nav />
    <nuxt />
    <the-footer />
  </div>
</template>

<script>
import TheNav from '@/components/Nav/TheNav'
import TheFooter from '@/components/Nav/TheFooter'
export default {
  components: {
    TheNav,
    TheFooter
  },
  created () {

  }
}
</script>
