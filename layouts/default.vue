<template>
  <div>
    <header>
      <nav>
        <v-row justify="center" no-gutters>
          <NuxtLink v-slot="{ navigate }" to="/about">
            <v-btn
              color="white"
              class="mx-2"
              text="About"
              @click="navigate"
            />
          </NuxtLink>
          <NuxtLink v-slot="{ navigate }" to="/">
            <v-btn
              color="white"
              class="mx-2"
              text="Home"
              @click="navigate"
            />
          </NuxtLink>
          <NuxtLink v-slot="{ navigate }" to="/posts">
            <v-btn
              color="white"
              class="mx-2"
              text="Posts"
              @click="navigate"
            />
          </NuxtLink>
        </v-row>
        <v-divider class="mt-2" />
      </nav>
    </header>
    <AppHeader />
    <slot />
    <AppFooter />
  </div>
</template>
<script setup lang="ts">
</script>
<style scoped>
</style>
