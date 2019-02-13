<template>
    <div class="container">
        <table class="table centered">
            <tbody>
                <tr>
                    <th width="50%" style="text-align: center">Title</th>
                    <th width="50%" style="text-align: center">Description</th>
                </tr>
                <tr v-if="title || description">
                    <td>{{ title }}</td>
                    <td>{{ description }}</td>
                </tr>
            </tbody>
        </table>
    </div>
</template>

<script>
    // import { EventBus } from '../main.js';

    export default {

        data() {
            return {
                title: '',
                description: ''
            }
        },
        mounted() {
            this.$eventBus.$on('emitted-data', ({ title, description}) => {
                this.title = title;
                this.description = description
            })
        }
    }
</script>

<style scoped>

</style>