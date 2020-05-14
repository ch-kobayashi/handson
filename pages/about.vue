<template lang="html">
    <nuxt-link to="/">TOP</nuxt-link>
</template>

<script>
export default {
    head() {
        return {
            title: 'This is ABOUT Page!!',
            meta: [
                { hid: 'description', name: 'description', content: 'aboutページ'}
            ]
        }
    },
    layout: 'dark'
}
</script>

<style lang="css">

</style>