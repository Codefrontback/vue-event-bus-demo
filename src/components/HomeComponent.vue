<template>
    <div class="row">
        <div class="container">
            <div>
                <center><h5>Article</h5></center>
            </div>
            <div class="col s12">
                <div class="row">
                    <div class="input-field col s12">
                        <input id="title" type="text" class="validate" v-model="article.title">
                        <label for="title">Title</label>
                    </div>
                </div>
                <div class="row">
                    <div class="input-field col s12">
                        <textarea id="description" class="materialize-textarea" data-length="120" v-model="article.description"></textarea>
                        <label for="description">Description</label>
                    </div>
                </div>
                <button class="btn btn-block waves-effect waves-light submit" type="button" name="action" @click="submit()">Emit Data</button>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        data() {

            return {
                article: {
                    title: '',
                    description: ''
                }
            }

        },

        methods: {
            submit() {
                this.$eventBus.$emit('emitted-data', this.article);
                this.article = { };
            }
        }
    }
</script>

<style scoped>

</style>