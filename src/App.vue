<template>
    <div class="container mt-10">

        <app-header :quoteCount="quotes.length" :maxQuotes="maxCount"></app-header>

        <app-add-quots @addQuote="newQuots"></app-add-quots>

        <app-quots-grid :quots="quotes"></app-quots-grid>
    </div>

</template>

<script>
    import QuotsGrid from './components/QuotsGrid.vue';
    import AddQuots from './components/AddQuots.vue';
    import Header from './components/Header.vue';
export default {
    data() {
        return {
            quotes :['1 quots'],
            maxCount: 15,

        }
    },
    components: {
        appQuotsGrid: QuotsGrid,
        appAddQuots: AddQuots,
        appHeader: Header,
    },
    methods: {
        newQuots(quote) {
            this.quotes.push(quote);
        }
    }
}
</script>

<style>
    .box_one{
        background-color: aliceblue;
        border: 1px solid black;
        box-shadow: 1px 1px 2px black;
        padding: 30px ;
        text-align: center;
        cursor: pointer;
    }
    .box_one:hover {
        background-color: bisque;
    }
    .mt-10 {
        margin-top: 30px;
    }
</style>
