<template>
    <div class="card">
        <div class="card-body">
            {{ data.image }} <br>
            {{ data.name }} <br>
            {{ data.price }} <br>
            {{ data.category }}
        </div>
    </div>
</template>
<script setup lang="ts">
import { defineProps } from 'vue';
import type { Product } from './types';

defineProps<{
  data: Product
}>()

</script>