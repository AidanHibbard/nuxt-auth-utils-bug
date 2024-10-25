<template>
  <header>
    <p class="underline">Welcome!</p>
    <AuthState>
      <template #default="{ loggedIn, clear }">
        <button v-if="loggedIn" @click="clear">Logout</button>
        <NuxtLink v-else to="/auth/auth0">Login</NuxtLink>
      </template>
      <template #placeholder>
        <button disabled>Loading...</button>
      </template>
    </AuthState>
  </header>
</template>
