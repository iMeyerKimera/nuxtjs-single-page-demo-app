<template>
  <article class="product">
    <!-- bind style for background image to a dynamic value-->
    <div class="thumbnail" :style="{backgroundImage: 'url(' + thumbnail + ')'}"></div>
    <h1>{{title}}</h1>
    <p>{{previewText}}</p>
  </article>
</template>

<script>
  export default {
    props: ['thumbnail', 'title', 'previewText']
  }
</script>


