<template>
  <header>
    <div class="container">
      <img src="../assets/img/dc-logo.png" alt="">
      <nav>
        <ul>
          <li v-for= "(link,index) in links" :key= "index">
            <a href="#">{{links[index].text}}</a>
          </li>
        </ul>
      </nav>
    </div>
  </header>
</template>

<script>
export default {
  name: 'Header',
  data () {
    return {
      links: [
        {text: "CHARACTERS"},
        {text: "COMICS"},
        {text: "MOVIES"},
        {text: "TV"},
        {text: "GAMES"},
        {text: "COLLECTIBLES"},
        {text: "VIDEOS"},
        {text: "FANS"},
        {text: "NEWS"},
        {text: "SHOP"}
      ]
    }
  }
}
</script>

<style scoped lang="scss">
@import "../style/variables";
@import "../style/mixins";

header {
  padding: 20px 0;
  .container {
    @include container;
    display: flex;
    justify-content: space-between;
  
    img {
      height: 60px;
    }
  
    nav {
      @include list-style-none;
      ul {
        display: flex;
        justify-content: space-between;
        align-items: center;
        height: 100%;
        li {
          margin: 0 10px;
          a {
            font-size: 11px;
            font-weight: 600;
            color: $text-black;
          }
        }
      }
    }
  }
}
</style>
