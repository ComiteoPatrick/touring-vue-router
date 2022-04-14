<template>
  <p>Register for event here</p>
  <button @click="register">Register Me</button>
</template>

<script>
export default {
  name: 'EventRegister',
  props: {
    event: {
      type: Object,
    },
  },
  inject: {
    GStore: {
      type: String,
    },
  },
  methods: {
    register() {
      this.GStore.flashMessage =
        'You are successfully registered for ' + this.event.title

      setTimeout(() => {
        this.GStore.flashMessage = ''
      }, 3000)
      /**
       * Natural solution:
       */
      this.$router.push({
        name: 'EventDetails',

        /**
         * passing id is optionnal here because router is retrieved by the router
         */
        // params: { id: this.event.id },
      })
    },
  },
}
</script>

<style scoped></style>
