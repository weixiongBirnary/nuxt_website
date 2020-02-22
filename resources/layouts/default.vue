<template>
  <div>
    <top-header></top-header>
    <main id="main" role="main">
      <nuxt></nuxt>
    </main>
    <bottom-footer></bottom-footer>
  </div>
</template>

<script>
import TopHeader from '../components/TopHeader'
import BottomFooter from '../components/BottomFooter'
export default {
  components: {
    TopHeader,
    BottomFooter
  }
}
</script>
<style lang="sass">
@import '../assets/scss/styles.scss'
</style>