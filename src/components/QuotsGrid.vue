<template>
    <div>
        <app-quots-grid v-for="(quote, index) in quots" @click.native="deleteQuotes(index)">{{ quote }}</app-quots-grid>
    </div>

</template>

<script>
    import Quots from './Quots.vue'
    export default {
        props: ['quots'],

        components: {
            appQuotsGrid: Quots,
        },
        methods: {
            deleteQuotes(index) {
                this.quots.splice(index, 1);
            }
        }

    }
</script>

<style>

</style>