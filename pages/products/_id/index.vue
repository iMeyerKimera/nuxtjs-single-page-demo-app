<template>
  <section class="product-view">
    <h1>{{product.title}}</h1>
    <div>
      <img class="product-media" :src="product.thumbnail" :alt="product.title">
    </div>
    <p>{{product.descriptionText}}</p>

<!-- Initial object properties-->
<!--    <h1>{{$route.params.id}}</h1>-->
<!--    <div>-->
<!--      <img src="" alt="">-->
<!--    </div>-->
<!--    <p>The product description.</p>-->
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

<script>
  export default {
  asyncData(context) {
      return new Promise((resolve, reject) => {
        setTimeout(() => {
          resolve({
            product: [
              {
                id: "1",
                title: "5-HTP SUPREME™",
                previewText: "5•HTP Supreme™ is a synergistic formula of 5-hydroxytryptophan (100 mg)",
                descriptionText: "5•HTP Supreme™ is a synergistic formula of 5-hydroxytryptophan (100 mg) and vitamin B6 (20 mg) for supporting overall neurotransmitter metabolism by providing precursors of serotonin. 5-HTP readily enters the blood brain barrier, however conversion into serotonin requires the cofactor vitamin B6, which is included in this formula. 5•HTP Supreme™ may be used during the day to support healthy mood or appetite, or at bedtime to support sleep.**\n" +
                  "\n" +
                  "\n" +
                  "This formula can be used in place of 5•HTP Synergy™ when higher doses of 5-HTP are recommended.",
                thumbnail: "https://shop.designsforhealth.com/assets/images/items/5htp-supreme_60%20capsules-1.png?resizeid=7&resizeh=500&resizew=500"
              },
              {
                id: "2",
                title: "5-HTP SYNERGY™",
                previewText: "5•HTP Synergy™ is a synergistic formula of 5-hydroxytryptophan and vitamin",
                descriptionText: "5•HTP Synergy™ is a synergistic formula of 5-hydroxytryptophan and vitamin B6 for supporting overall neurotransmitter metabolism by providing precursors of serotonin. 5-HTP readily enters the blood brain barrier; however, conversion into serotonin requires the cofactor vitamin B6, which is included in this formula. 5•HTP Synergy™ may be used during the day to support healthy mood or appetite, or at bedtime to support sleep.**",
                thumbnail: "https://shop.designsforhealth.com/assets/images/items/5htp-synergy_90%20capsules-1.png?resizeid=7&resizeh=500&resizew=500"
              },
              {
                id: "3",
                title: "7-KETO®",
                previewText: "7-Keto® is a registered trade name for the compound 3-acetyl-7-oxo DHEA",
                descriptionText: "7-Keto® is a registered trade name for the compound 3-acetyl-7-oxo DHEA, a stabilized form of 7-oxo DHEA. Once ingested, acetyl-7-oxo DHEA is cleaved to 7-oxo DHEA, a DHEA metabolite naturally found in the body.\n" +
                  "\n" +
                  "\n" +
                  "Supplementation with 7-Keto® may counteract the decline in 7-oxo DHEA levels that occurs during the normal aging process. Although 7-oxo DHEA is similar to DHEA, it does not convert into estrogenic or androgenic hormones.\n" +
                  "\n",
                thumbnail: "https://shop.designsforhealth.com/assets/images/items/7-keto_60%20capsules-1.png?resizeid=7&resizeh=500&resizew=500"
              }
            ].find(el => el.id === context.params.id)  // This executes to each element in the product objects and returns the right one
            // with the object whose context is the element id.
          })
        }, 1500)
      })
    },
  }
</script>

<style scoped>
  .product-view {
    display: flex;
    flex-flow: column;
    justify-content: center;
    align-items: center;
    text-align: center;
    padding: 30px;
  }
  .product-media {
    width: 100%;
  }
</style>
