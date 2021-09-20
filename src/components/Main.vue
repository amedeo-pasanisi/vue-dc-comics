<template>
  <main>
    <div class="top">
        <div class="container">
            <h1>Main top</h1>
        </div>
    </div>
    <div class="bottom">
        <div class="container">
            <h1>Main bottom</h1>
        </div>
    </div>
  </main>
</template>

<script>
export default {
  name: 'Main',
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
    .container {
    @include container;
    display: flex;
    align-items: center;
    height: 100px;
    }
}
</style>
