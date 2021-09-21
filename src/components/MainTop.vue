<template>
    <section class="top">
        <div class="jumbotron">
            <img src="@/assets/img/jumbotron.jpg" alt="">
        </div>
        <ul class="cardsContainer">
            <button>
                <h1>CURRENT SERIES</h1>
            </button>
            <ComicCard
                v-for="(comic, index) in comics"
                :key= "index"
                :comicCard= "comic"
            />
        </ul>
        <button>LOAD MORE</button>
    </section>
</template>

<script>
import comics from "@/data/dc-comics.json";
import ComicCard from "./ComicCard"

export default {
    name: 'MainTop',
    components: {
        ComicCard
    },
    data() {
        return {
            comics
        }
    }
}
</script>

<style scoped lang="scss">
@import "../style/variables";
@import "../style/mixins";

.top {
    display: flex;
    flex-direction: column;
    align-items: center;
    padding-bottom: 20px;
    background-color: rgb(29, 29, 29);
    color: white;
    .jumbotron {
        height: 300px;
        overflow: hidden;
        margin-bottom: 20px;
        img {
            width: 100%;
        }
    }
    @include list-style-none;
    ul.cardsContainer {
        @include container;
        position: relative;
        display: flex;
        flex-wrap: wrap;
        button {
            position: absolute;
            top: -40px;
            left: 10px;
        }
    }
    button {
        padding: 10px 30px;
        border: none;
        color: white;
        font-weight: 600;
        font-size: 11px;
        background-color: $blue;
    }
}
</style>