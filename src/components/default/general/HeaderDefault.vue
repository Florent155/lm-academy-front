<template>
  <header>
    <div class="flex justify-between items-center border-b-textPrimary border-b-4 py-4">
      <h1 class="logo text-5xl text-textPrimary">Lm Academy</h1>
      <nav class="text-3xl flex gap-2">
        <router-link
          to="/"
          class="hover:underline"
          :class="{ underline: $route.path === '/' }"
        >
          Home
        </router-link>
        |
        <router-link
          to="/about-us"
          class="hover:underline"
          :class="{ underline: $route.path === '/about-us' }"
        >
          About us
        </router-link>
        |
        <router-link
          to="/login"
          class="hover:underline"
          :class="{ underline: $route.path === '/login' }"
        >
          Login
        </router-link>
      </nav>
    </div>
  </header>
</template>
