<template>
    <div>
        <table class="table">
            <thead>
                <tr>
                <th scope="col">Title</th>
                <th scope="col">Year</th>
                <th scope="col">Time</th>
                <th scope="col">Genre</th>
                </tr>
            </thead>
            <tbody>
                <tr v-for="song in props.songs">
                <td>{{ song.TITLE }}</td>
                <td>{{ song.YEAR }}</td>
                <td>{{ song.TIME }}</td>
                <td>{{ song.GENRE }}</td>
                </tr>

            </tbody>
        </table>
    </div>
</template>

<script setup>
const props = defineProps(['songs']);

</script>

<style scoped>

</style>