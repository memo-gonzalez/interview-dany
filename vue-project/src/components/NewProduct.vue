<template>
    <div>
        <div class="form-group">
            <label for="">Image</label>
            <input type="text" v-model="image" class="form-control">
        </div>
        <div class="form-group">
            <label for="">Name</label>
            <input type="text" v-model="name" class="form-control">
        </div>
        <div class="form-group">
            <label for="">Price</label>
            <input type="text" v-model="price" class="form-control">
        </div>
        <div class="form-group">
            <label for="">Persona</label>
            <input type="text" v-model="persona" class="form-control">
        </div>
        <button @click="Add" class="btn btn-primary">Add Item</button>
    </div>
</template>
<script setup lang="ts">
import { ref } from 'vue';
const image = ref('');
const name = ref('');
const price = ref('');
const persona = ref('');

defineEmits(['newItem'])

</script>