<template>
  <div class="fluid-container">
    <SalesLandingHeader />
    <SalesLandingContent />
    <SalesLandingFooter />
  </div>
</template>

<script>
import SalesLandingHeader from '../components/SalesPage/SalesLandingHeader'
import SalesLandingContent from '../components/SalesPage/SalesLandingContent'
import SalesLandingFooter from '../components/SalesPage/SalesLandingFooter'

export default {
  components: {
    SalesLandingHeader,
    SalesLandingContent,
    SalesLandingFooter
  }
}
</script>

<style>

</style>
