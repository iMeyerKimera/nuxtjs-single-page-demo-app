<template>
  <nuxt-link :to="'/products/' + id ">
  <!-- To out put a link that uses the id, we'll wrap the article element inside the nuxt-link component
        which uses the route link behind the scenes.
  -->
    <article class="product">
      <!-- bind style for background image to a dynamic value-->
      <div class="thumbnail" :style="{backgroundImage: 'url(' + thumbnail + ')'}"></div>
      <h1>{{title}}</h1>
      <p>{{previewText}}</p>
    </article>
  </nuxt-link>
<!--  <article class="product">-->
<!--    &lt;!&ndash; bind style for background image to a dynamic value&ndash;&gt;-->
<!--    <div class="thumbnail" :style="{backgroundImage: 'url(' + thumbnail + ')'}"></div>-->
<!--    <h1>{{title}}</h1>-->
<!--    <p>{{previewText}}</p>-->
<!--  </article>-->
</template>

<script>
  //
  export default {
    props: ['thumbnail', 'title', 'previewText', 'id']
  }
</script>

<style scoped>
  a {
    text-decoration: none;
    color: black;
  }
  .product {
    box-sizing: border-box;
    width: 280px;
    padding: 8px;
    border: 1px solid #ccc;
    box-shadow: 0 2px 2px #aaa;
    margin: 10px;
  }
  .thumbnail {
    background-position: center;
    background-size: cover;
    width: 100%;
    height: 200px;
  }
</style>


