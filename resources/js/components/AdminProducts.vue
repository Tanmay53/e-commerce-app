<template>
  <div>
      <h1>Products</h1>
      <ol>
          <div v-for="(product, id) in products" v-bind:key="id" class="w-100 d-flex">
              {{ (id + 1) + ". " + product.name + " &#8377;" + product.price }}
              <div class="flex-grow-1"></div>
              <button :id="'remove-' + product.id" class="">Remove</button>
              <button :id="'edit-' + product.id" class="">Edit</button>
          </div>
      </ol>
  </div>
</template>

<script>
export default {
    data() {
        return {
            products: [
                {
                    'name': "ABC",
                    'price': "120"
                },
                {
                    'name': "DEF",
                    'price': "120"
                },
                {
                    'name': "GHI",
                    'price': "120"
                },
                {
                    'name': "JKL",
                    'price': "120"
                }
            ]
        };
    }
}
</script>

<style>

</style>
