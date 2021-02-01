<template>
  <div class="container">
    <div>
      <nuxt-link to="/textcloud"
        class="text-white bg-blue-500 hover:bg-blue-700 py-3 px-4 font-semibold rounded-lg shadow-md">TextCloud
      </nuxt-link>
    </div>
  </div>
</template>

<script>
  export default {

  }

</script>

<style lang="scss" scoped>
  .container {
    margin: 0 auto;
    min-height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
    text-align: center;
    font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
      'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  }

</style>
