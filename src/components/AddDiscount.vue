<template>
  <div>
    <h1>Hello World</h1>
    <h1>Hello World</h1>
    <h1>{{ productsWithDiscount }}</h1>
  </div>
</template>

<script>
import { ref, computed } from 'vue'
export default {
  props: {
    products: { type: Object, default: () => ({}) }
  },
  setup(props){

    const copyProducts = ref(props.products)

    const productsWithDiscount = computed(() => {
      return copyProducts.value.map(item => ({...item, ...{discount: item.price > 20000 ? 20 : 5}}))
    })

    return {copyProducts, productsWithDiscount}
  }
}
</script>
