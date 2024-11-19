<template>
    <div class="container">
        <ProductItem v-for="(item, index) in list" :key="index"
            :data="item"/>

        <NewProduct/>
        <button class="btn btn-primary"@click="addProduct">Add Item</button>
    </div>

</template>

<script setup lang="ts">
import { ref } from 'vue';
import ProductItem from './ProductItem.vue';
import NewProduct from './NewProduct.vue';
import type { Product } from './types'; 
//image, name, price,category
const list = ref<Product[]>([
    {
        image: 'product1.png',
        name: 'Reloj de mano',
        price: 20,
        category: 'personal'
    },
    {
        image: 'product2.png',
        name: 'Televisor',
        price: 400,
        category: 'home'
    },
])

const addProduct = () => {
    const newItem:Product = {
        image: '',
        name: '',
        price: 0,
        category: 'other'
    }
    list.value.push(newItem)
}
</script>