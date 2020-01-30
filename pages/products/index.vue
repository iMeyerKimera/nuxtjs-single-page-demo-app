<template>
  <section class="products">
    <article class="product">
      <div class="thumbnail" style="background-image: url('https://shop.designsforhealth.com/assets/images/items/5htp-supreme_60%20capsules-1.png?resizeid=7&resizeh=500&resizew=500')"></div>
      <h1>5-HTP SUPREME™</h1>
      <p>5•HTP Supreme™ is a synergistic formula of 5-hydroxytryptophan (100 mg)</p>
    </article>
    <article class="product">
      <div class="thumbnail" style="background-image: url('https://shop.designsforhealth.com/assets/images/items/5htp-synergy_90%20capsules-1.png?resizeid=7&resizeh=500&resizew=500')"></div>
      <h1>5-HTP SYNERGY™</h1>
      <p>5•HTP Synergy™ is a synergistic formula of 5-hydroxytryptophan and vitamin</p>
    </article>
    <article class="product">
      <div class="thumbnail" style="background-image: url('https://shop.designsforhealth.com/assets/images/items/7-keto_60%20capsules-1.png?resizeid=7&resizeh=500&resizew=500')"></div>
      <h1>7-KETO®</h1>
      <p>7-Keto® is a registered trade name for the compound 3-acetyl-7-oxo DHEA</p>
    </article>
  </section>
</template>

<style scoped>
  .products {
    display: flex;
    flex-flow: row wrap;
    justify-content: center;
    align-items: center;
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
