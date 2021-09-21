<template>
    <li>
        <img :src="comicCard.thumb" alt="">
        <div>{{comicCard.series}}</div>
    </li>
</template>

<script>
export default {
    name: "ComicCard",
    props: ["comicCard"]
}
</script>

<style>

</style>