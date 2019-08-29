<template>
    <div>
        <form action="" >
            <div class="row">
                <div class="form-group col-md-8 col-offset-2">
                    <label>Create New Quots</label>
                    <textarea cols="30" rows="10" class="form-control" v-model="quote"></textarea>
                </div>
                <div class="form-group col-md-8 col-offset-2">
                    <button class="btn btn-primary" @click.prevent="createNew">Create New</button>
                </div>
            </div>
        </form>
    </div>

</template>

<script>
    export default {
        data() {
            return {
                quote: ''
            };
        },
        methods: {
            createNew() {
                this.$emit('addQuote', this.quote);
                this.quote = '';
            }
        },
    }
</script>

<style>

</style>