<template>
  <section class="products">
    <!-- Bind to a product object -->
    <Product
      v-for="product in products"
      :key="product.id"
      :thumbnail="product.thumbnail"
      :title="product.title"
      :preview-text="product.previewText"
      :id="product.id"
    />

<!--  Second Products page instances concept  -->
<!--    <Product-->
<!--      thumbnail="https://shop.designsforhealth.com/assets/images/items/5htp-supreme_60%20capsules-1.png?resizeid=7&resizeh=500&resizew=500"-->
<!--      title="5-HTP SUPREME™"-->
<!--      preview-text="5•HTP Supreme™ is a synergistic formula of 5-hydroxytryptophan (100 mg)"-->
<!--      id="1"-->
<!--    />-->
<!--    <Product-->
<!--      thumbnail="https://shop.designsforhealth.com/assets/images/items/5htp-synergy_90%20capsules-1.png?resizeid=7&resizeh=500&resizew=500"-->
<!--      title="5-HTP SYNERGY™"-->
<!--      preview-text="5•HTP Synergy™ is a synergistic formula of 5-hydroxytryptophan and vitamin"-->
<!--      id="2"-->
<!--    />-->
<!--    <Product-->
<!--      thumbnail="https://shop.designsforhealth.com/assets/images/items/7-keto_60%20capsules-1.png?resizeid=7&resizeh=500&resizew=500"-->
<!--      title="7-KETO®"-->
<!--      previewText="7-Keto® is a registered trade name for the compound 3-acetyl-7-oxo DHEA"-->
<!--      id="3"-->
<!--    />-->

<!-- Initial Products Page Instances Concept   -->
<!--    <article class="product">-->
<!--      <div class="thumbnail" style="background-image: url('https://shop.designsforhealth.com/assets/images/items/5htp-supreme_60%20capsules-1.png?resizeid=7&resizeh=500&resizew=500')"></div>-->
<!--      <h1>5-HTP SUPREME™</h1>-->
<!--      <p>5•HTP Supreme™ is a synergistic formula of 5-hydroxytryptophan (100 mg)</p>-->
<!--    </article>-->
<!--    <article class="product">-->
<!--      <div class="thumbnail" style="background-image: url('https://shop.designsforhealth.com/assets/images/items/5htp-synergy_90%20capsules-1.png?resizeid=7&resizeh=500&resizew=500')"></div>-->
<!--      <h1>5-HTP SYNERGY™</h1>-->
<!--      <p>5•HTP Synergy™ is a synergistic formula of 5-hydroxytryptophan and vitamin</p>-->
<!--    </article>-->
<!--    <article class="product">-->
<!--      <div class="thumbnail" style="background-image: url('https://shop.designsforhealth.com/assets/images/items/7-keto_60%20capsules-1.png?resizeid=7&resizeh=500&resizew=500')"></div>-->
<!--      <h1>7-KETO®</h1>-->
<!--      <p>7-Keto® is a registered trade name for the compound 3-acetyl-7-oxo DHEA</p>-->
<!--    </article>-->
  </section>
</template>

<script>
// Imported and registered the product component into the products index.vue file.
// This gives you direct access to this component and also provides access to the products instances
// import Product from '@/components/Recipe'
import Product from '../../components/Product';

export default {
  components: {
    Product
  },
  // Simulate serving data from a server
  // This asyncData is a special method executes on the server whenever request is made
  // When you are on a single page mode and clicking around, it executes on the client, but if you send
  // a request initially, it executes on the server to fetch all the data that needs to be rendered on the page
  // in advance on the server, before returning the page so you can pre-render the page with the data
  // on the server, and then send back the finished page to the user
  //
  asyncData() {
    // return axios.get()
    // Let's perform a face request to resolve data with asyncData but in reality, you would want to use
    // some method such as axios.get()
    return new Promise((resolve, reject) => {
      setTimeout(() => {
        resolve({
          products: [
            {
              id: "1",
              title: "5-HTP SUPREME™",
              previewText: "5•HTP Supreme™ is a synergistic formula of 5-hydroxytryptophan (100 mg)",
              thumbnail: "https://shop.designsforhealth.com/assets/images/items/5htp-supreme_60%20capsules-1.png?resizeid=7&resizeh=500&resizew=500"
            },
            {
              id: "2",
              title: "5-HTP SYNERGY™",
              previewText: "5•HTP Synergy™ is a synergistic formula of 5-hydroxytryptophan and vitamin",
              thumbnail: "https://shop.designsforhealth.com/assets/images/items/5htp-synergy_90%20capsules-1.png?resizeid=7&resizeh=500&resizew=500"
            },
            {
              id: "3",
              title: "7-KETO®",
              previewText: "7-Keto® is a registered trade name for the compound 3-acetyl-7-oxo DHEA",
              thumbnail: "https://shop.designsforhealth.com/assets/images/items/7-keto_60%20capsules-1.png?resizeid=7&resizeh=500&resizew=500"
            }
          ]
        })
      }, 1500)
    })
  },

}
</script>

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
