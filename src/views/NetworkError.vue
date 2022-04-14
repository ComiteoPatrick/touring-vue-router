<template>
  <div class="network-error">
    <h1>Uh-Oh!</h1>
    <h3>
      <p>It looks like you're experiencing some network issues.</p>
      <p>
        Please take a deep breath and
        <a href="#" @click="this.$router.go(-1)">Click here</a> to try again
      </p>
    </h3>
  </div>
</template>

<style scoped>
.network-error {
}
</style>
