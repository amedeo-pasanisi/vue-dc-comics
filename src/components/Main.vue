<template>
  <main>
    <div class="top">
        <ul class="container">
            <ComicCard
                v-for="(comic, index) in comics"
                :key= "index"
                :comicCard= "comic"
            />
        </ul>
    </div>
    <div class="bottom">
        <div class="container">
            <h1>Main bottom</h1>
        </div>
    </div>
  </main>
</template>

<script>
import comics from "@/data/dc-comics.json";
import ComicCard from "./ComicCard"

export default {
    name: 'Main',
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

main {
    .top {
        padding: 20px 0;
        background-color: black;
        color: white;
    }
    .bottom {
        padding: 20px 0;
        background-color: $blue;
        color: white;
    }
    
    @include list-style-none;
    .container {
        @include container;
        display: flex;
        align-items: center;
        flex-wrap: wrap;
    }
}
</style>
