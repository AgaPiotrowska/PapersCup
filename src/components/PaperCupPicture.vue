<template>
    <img :src="Image" alt="Paper Cup" width="800" height="406"/>
</template>

<script>
import Image from '../assets/papercup.png';

export default {
    name: 'PaperCupPicture',

    data() {
        return {
            Image,
        }
    }
}

</script>

<style lang="scss" scoped>

</style>