<template lang="html">
    <div class="sample">
        <div class="slot">
            <slot name="slot2" />
        </div>
        <div>
            <h1>{{ title }}</h1>
            Hello, I'm {{ name }} 
        </div>
        <div>
            {{ reverseName }}
        </div>
        <button type="button" name="button" v-on:click="plus">click times: {{ num }}</button>
        <div :class="['hide', { three: num !== 0 && num % 3 === 0 }]">
            AHOOOO!
        </div> 
        <div class="slot">
            <slot name="slot1" />
        </div>
    </div>
</template>

<script>
export default {
    props: {
        title: {
            type: String,
            default: 'Default Title'
        }
    },
    data() {
        return {
            name: 'hashi-chia',
            num: 0
        }
    },
    methods: {
        plus() {
            this.num++
        }
    },
    computed: {
        reverseName() {
            return this.name.split('').reverse().join('')
        }
    },
    mounted() {
        console.log('mounted!')
    }
}
</script>

<style lang="scss" scoped>
.hide {
    display: none;
    &.three {
        display: block;
    }
}

.slot {
    color: red;
}
</style>