<template>
    <div class="wrapper">
        <scroller>
            <product :products="goods"></product>
        </scroller>
    </div>
</template>

<style scoped>
.wrapper {
  background-color: #f3f4f5;
  /* background: red; */
}
</style>

<script>
import productData from "./productData";
import product from "./product.vue"

export default {
  components: {
    product
  },
  data() {
    return {
      goods: productData
    };
  }
};
</script>