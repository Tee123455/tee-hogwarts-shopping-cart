<template>
  <div>
    <CartListitem
      v-for="cartItem in cartItems"
      :key="cartItem.id"
      :item="cartItem"
      @item-remove="$emit('item-remove', $event)"
      @quantity-update="$emit('quantity-update', $event)"
    ></CartListitem>
  </div>
</template>

<script setup>
import CartListitem from '@/components/CartListitem.vue'
defineProps(['cartItems'])
defineEmits(['item-remove', 'quantity-update'])
</script>

<style scoped></style>