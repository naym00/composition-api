<template>
  <div>
    <add-discount :products="products"/>
  </div>
</template>

<script>
import AddDiscount from '../components/AddDiscount.vue'
import { ref } from 'vue'

export default {
  name: 'Home',
  components: { 'add-discount': AddDiscount },
  setup(){
    const products = ref([
      { id: 1, name: 'Computer', price: 50000, rating: 4 },
      { id: 2, name: 'Mobile', price: 20000, rating: 3 },
      { id: 3, name: 'Car', price: 500000, rating: 5 },
      { id: 4, name: 'Laptop', price: 60000, rating: 3 },
      { id: 5, name: 'Mouse', price: 1000, rating: 5 }
    ])

    return { products }
  }
}
</script>