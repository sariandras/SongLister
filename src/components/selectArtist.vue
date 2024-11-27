<template>
    <div>
        <label for="SelectArtist">Artist:</label>
        <select class="form-select" id="selectArtist" @change="changeArtist($event)">
            <option selected>Select an artist</option>
            <option v-for="artist in props.artists" :value="artist._id">{{artist.artist}}</option>
        </select>
    </div>
</template>

<script setup>
const props = defineProps(['artists'])
const emits = defineEmits(['changeArtist'])

const changeArtist = (event)=>{
    const selectedArtistId = event.target.value;
    emits('changeArtist',selectedArtistId)
}
</script>

<style scoped>

</style>