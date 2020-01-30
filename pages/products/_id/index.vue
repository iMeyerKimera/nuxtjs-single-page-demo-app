<template>
  <section class="product-view">
    <h1>{{$route.params.id}}</h1>
    <div>
      <img src="" alt="">
    </div>
    <p>The product description.</p>
  </section>
</template>

<style scoped>
  .product-view {
    display: flex;
    flex-flow: column;
    justify-content: center;
    align-items: center;
    text-align: center;
    padding: 30px;
  }
</style>
