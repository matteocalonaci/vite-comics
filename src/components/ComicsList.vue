<script>
export default {
    name: "ComicsList",
    props: ["fumetti"],
    data() {
        return {

        }
    }
}
</script>

<template>
    <div class="card col-2">
        <img :src="fumetti.thumb" alt="">
        <p class="text-white">{{ fumetti.series }}</p>

    </div>
</template>

<!-- CSS -->
<style scoped>
.col-2 {
    background: #222;
    border: none;
}

/* BORDO MESSO A CASO IN AUTOMATICO?? */

.col-2 img {
    height: 12rem;
    width: 12rem;

}

.row {
    padding-top: 2rem;
}
</style>