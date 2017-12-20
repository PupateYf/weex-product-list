<template>
  <div class="wraper">
      <div class="product-list-holder">
          <div class="product-item" v-for="item in products">
              <image class="product-image" resize="cover" :src="item.small_image"></image>
              <div class="product-info">
                  <div class="price-holder">
                      <text class="product-price">¥{{item.vipshop_price}}</text><text class="product-off-price">一口价</text>
                  </div>
                  <text class="product-name">{{item.product_name}}</text>
              </div>
          </div>
      </div>
  </div>

</template>

<style scoped>
.wrapper{
  width: 750px;
}
.product-list-holder {
  padding: 0 14px;
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  justify-content: space-between;
}
.product-item {
  width: 354px;
  height: 640px; 
  margin-bottom: 14px;
  background-color: #fff
}
.product-image {
  width: 350px;
  height: 440px;
}
.product-name {
  font-size: 24px;
  display: block;
  margin-top: 30px;
  lines: 2;
  color: #585c64;
  text-overflow: ellipsis;
}
.product-info {
  padding: 30px 20px 0 20px;
}
.price-holder {
  flex-direction: row;
}
.product-price {
  font-size: 30px;
  line-height: 30px;
  color: black;
  overflow: hidden;
  lines: 1;
  white-space: nowrap;
  text-overflow: ellipsis;
}
.product-off-price {
  margin-left: 20px;
  color: #98989f;
  font-size: 25px;
  line-height: 30px;
}
</style>

<<script>
export default {
  name: 'Product',
  props: ['products']
}
</script>

