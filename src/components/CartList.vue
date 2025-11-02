<template>
    <div>
        <CartListItem
        v-for="cartItem in cartItems"
        :key="cartItem.id"
        :item="cartItem"
        @item-remove="$emit('item-remove', $event)"
        @update-quantity="$emit('update-quantity', $event)"
        ></CartListItem>
    </div>

</template>

<script setup>
import CartListItem from './CartListItem.vue';

defineProps(['cartItems']);
defineEmits(['item-remove', 'update-quantity']);
</script>

<style scoped>

</style>