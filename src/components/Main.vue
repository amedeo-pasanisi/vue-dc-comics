<template>
  <main>
    <MainTop />
    <section class="bottom">
        <div class="container">
            <h1>Main bottom</h1>
        </div>
    </section>
  </main>
</template>

<script>
import MainTop from "./MainTop";

export default {
    name: 'Main',
    components: {
        MainTop
    },
}
</script>

<style scoped lang="scss">
@import "../style/variables";
@import "../style/mixins";

main {
    .bottom {
        padding: 20px 0;
        background-color: $blue;
        color: white;
    }
}
</style>
