<template>
  <div class="catalog-wrapper">
    <h2 class="title">Categories</h2>
    <catalog-main></catalog-main>
    <catalog-cart></catalog-cart>
  </div>
</template>

<script>
import CatalogCart from './CatalogCart.vue';
import CatalogMain from './CatalogMain.vue';

export default {
  components: { CatalogMain, CatalogCart },
};
</script>

<style lang="stylus">
.catalog-wrapper
  width 900
  margin 0 auto

.title
  font-size 30px
  text-align: center
</style>
