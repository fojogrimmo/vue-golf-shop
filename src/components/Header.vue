<script setup>
defineProps({
  totalPrice: Number
})
const emit = defineEmits(['openDrawer'])
</script>

<template>
  <header class="flex justify-between px-24 py-10 text-xl">
    <router-link to="/">
      <div class="flex items-center">
        <h2 class="text-4xl font-bold">3legant<span class="text-stone-500">.</span></h2>
      </div>
    </router-link>

    <ul class="flex items-center gap-10">
      <li
        @click="() => emit('openDrawer')"
        class="flex items-center gap-3 cursor-pointer hover:text-emerald-400 transition"
      >
        <img src="/cart.svg" alt="Cart" class="w-8" />
        <b>&#8364;{{ totalPrice }}</b>
      </li>
      <router-link to="/favorites">
        <li class="flex items-center gap-3 cursor-pointer hover:text-emerald-400 transition">
          <img src="/heart.svg" alt="Heart" class="w-6" />
          <span>Wishlist</span>
        </li>
      </router-link>

      <li class="flex items-center gap-3 cursor-pointer hover:text-emerald-400 transition">
        <img src="/profile.svg" alt="Profile" class="w-7" />
        <span>My Profile</span>
      </li>
    </ul>
  </header>
</template>
