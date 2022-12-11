<template>
    <div>
      <div class="container-fluid">
        <!-- side bar -->
        <div class="row">
          <ShoppingSidebar></ShoppingSidebar>
          <div class="col mt-5">
            <ShoppingCardVue></ShoppingCardVue>
          </div>
        </div>
      </div>
    </div>
  </template>
  <script>
  import ShoppingSidebar from './ShoppingSidebar.vue';
  import ShoppingCardVue from './ShoppingCard.vue';
  
  export default {
    name: 'ShopingHome',
    components: {
      ShoppingSidebar,
      ShoppingCardVue
    }
  
  }
  </script>
  <style scoped>
  .product-list .slide-box {
    border: 1px solid #fff;
    padding-bottom: 10px;
    margin: 15px 0;
    position: relative;
  }
  
  .product-section-main .product-list .product-box {
    position: relative;
    overflow: hidden;
  }
  
  .product-list .slide-box .size {
    opacity: 0;
    transition: all .5s;
  }
  
  body.w-store .product-section-main .product-list .product-box .view-detail {
    background: #c11d14;
    z-index: 99;
  }
  
  .product-section-main .product-list .slide-box:hover .view-detail {
    opacity: 1;
    bottom: 0;
  }
  
  .product-section-main .product-list .product-box .view-detail,
  .wordrobe-product .product-list .wordrobe-content .view-detail {
    color: #fff;
    font-size: 13px;
    line-height: 38px;
    width: 100%;
    text-align: center;
    text-transform: uppercase;
    text-decoration: none;
    transition: all .5s;
  }
  
  .product-section-main .product-list .product-box .view-detail {
    position: absolute;
    bottom: -58px;
    opacity: 0;
  }
  
  *,
  :after,
  :before {
    box-sizing: border-box;
  }
  
  a,
  button {
    outline: none !important;
    text-decoration: none;
  }
  </style>