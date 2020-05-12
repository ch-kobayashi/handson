<template>
  <div>
    <sample-component :title="indexTitle">
      <div slot="slot1">
        slot exsample
      </div>
      <div slot="slot2">
        slot exsample2
      </div>
    </sample-component>
    <nuxt-link to="/about">ABOUT</nuxt-link>
  </div>
  <!-- <sample-component /> -->
</template>

<script>
import SampleComponent from '~/components/SampleComponent.vue'
// import UpperCamelTest from '~/components/UpperCamelTest.vue'

export default {
  components: {
    SampleComponent
    // , UpperCamelTest
  },
  data() {
    return {
      indexTitle: 'Nuxt.js data'
    }
  }
}
</script>

<style>

</style>
