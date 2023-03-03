<template>
  <div class="catalog-item">
    <div class="catalog-item__img">
      <img :src="require(`@/assets/product/${item.image}`)" alt="">
    </div>
    <h4>{{ item.name }}</h4>
    <p>price: {{ item.price }}</p>
    <button @click="addCart">Add to cart</button>
  </div>
</template>

<script>
export default {
  props: {
    item: {
      type: Object,
    },
  },
  methods: {
    addCart() {
      this.$emit('addProduct', this.item.acticle);
    },
  },
};
</script>

<style lang="stylus">
.catalog-item
  width 300px
  height 300px
  text-align center
  border 1px solid burlywood
  padding 20px
  &__img
    width 260px
    margin 0 auto
    height 200px
    & img
      width 100%
      height 100%
      object-fit cover

</style>
