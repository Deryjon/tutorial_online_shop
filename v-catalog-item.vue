<template>
  <div class="v-catalog-item">
    <img class="v-catalog-item_image" :src=" require('../assets/images/' + product_data.image) " alt="img" />
    <p class="v-catalog-item_name">{{ product_data.name }}</p>
    <p class="v-catalog-item_price">Price: {{ product_data.price}} P.</p>
    <button class="v-catalog-item_add_to_cart_btn btn"
		@click="sendDataToParent"
		>Add to cart</button>
  </div>
</template>

<script>
export default {
  name: "v-catalog-item",
  props: {
    product_data: {
      type: Object,
      default() {
				return{}
			},
    },
  },
  data() {},
  computed: {},
	methods: {
		sendDataToParent() {
			this.$emit( "sendDataToParent", this.product_data.article)
		}
	}
};
</script>
<style lang="scss">
.v-catalog-item {
  flex-basis: 25%;
  box-shadow: 0 0 8px 0 #e0e0e0;
  padding: 16px;
  margin-bottom: 16px;
	&_image{
		width: 100px;
	}
}
</style>
