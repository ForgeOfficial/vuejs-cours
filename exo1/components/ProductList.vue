<template>
  <table border="1">
    <thead>
    <tr>
      <th>ID</th>
      <th>Label</th>
      <th>Description</th>
      <th>Statut</th>
    </tr>
    </thead>
    <tbody>
    <tr v-for="product in products" :key="product.id">
      <td>{{ product.id }}</td>
      <td>{{ product.label }}</td>
      <td>{{ product.description }}</td>
      <td>{{ getStatus(product.qty) }}</td>
    </tr>
    </tbody>
  </table>
</template>

<script setup lang="ts">
import type {Product} from "@/interface/product.interface.ts";

defineProps<{ products: Product[] }>()

const getStatus = (qty: number): string => {
  return qty > 0 ? 'Disponible' : 'Indisponible'
}
</script>
