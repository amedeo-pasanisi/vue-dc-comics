<template>
    <li>
        <div class="imgContainer">
            <img :src="comicCard.thumb" alt="">
        </div>
        <div>{{comicCard.series.toUpperCase()}}</div>
    </li>
</template>

<script>
export default {
    name: "ComicCard",
    props: ["comicCard"]
}
</script>

<style scoped lang="scss">
li {
    width: calc(100% / 6 - 20px);
    margin: 20px 10px 30px 10px;
    font-size: 11px;
    .imgContainer {
        width: 100%;
        height: 150px;
        overflow: hidden;
        margin-bottom: 20px;
        img {
            width: 100%;
        }
    }
}
</style>