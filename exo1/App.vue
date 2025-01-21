 <template>
  <div>
    <ProductList :products="products" />
  </div>
</template>

<script setup lang="ts">
import ProductList from './components/ProductList.vue'
import type {Product} from "@/interface/product.interface.ts";

const products: Product[] = [
  { id: 1, label: 'Carotte', description: 'de belles carottes', qty: 10 },
  { id: 2, label: 'Pomme', description: 'des pommes juteuses', qty: 0 },
  { id: 3, label: 'Poire', description: 'des poires mûres', qty: 5 },
]
</script>
