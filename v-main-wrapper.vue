<template>
  <div class="v-main-wrapper">
		<p>{{ title }}</p>
		<VCatalog />
		<VCart/>

	</div>
</template>

<script>
import VCart from './v-cart.vue';
import VCatalog from './v-catalog.vue';

export default {
	name: "v-main-wrapper",
	components:{ VCatalog, VCart },
	props:{},
	data() {
		return {
			title: "Main wrapper"
		}
	},
	computed:{},
	methods:{},
	watch:{},
	mounted(){
		console.log("Hello World");
	}
};
</script>
<style>
.v-main-wrapper {
  display: flex;
	flex-direction: column;
  justify-content: center;
  align-items: center;
  max-width: 900px;
  margin: 0 auto;
}
</style>
