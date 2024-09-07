<template>
  <div class="container">
    <div v-if="loading" class="loading-overlay">
      <div class="spinner"></div>
      <h1>Loading...</h1>
    </div>
    <div v-else>
      <h1>{{ message }}</h1>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      message: 'Welcome to my site',
      loading: true
    };
  },
  mounted() {
    setTimeout(() => {
      this.loading = false; 
    }, 3000); 
  }
};
</script>

<style>
</style>
