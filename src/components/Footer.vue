<template>
  <footer>
    <div class="top">
        <div class="container">
            <h1>footer top</h1>
        </div>
    </div>
    <div class="bottom">
        <div class="container">
            <h1>footer bottom</h1>
        </div>
    </div>
  </footer>
</template>

<script>
export default {
  name: 'Footer',
}
</script>

<style scoped lang="scss">
@import "../style/variables";
@import "../style/mixins";

footer {
    .top {
        padding: 20px 0;
        background-image: url("../assets/img/footer-bg.jpg");
        color: white;
    }
    .bottom {
        padding: 20px 0;
        background-color: $text-black;
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
