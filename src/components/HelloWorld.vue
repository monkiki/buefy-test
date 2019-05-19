<template>
  <div class="container">
    <section>
      <h1>{{ msg }}</h1>
      <b-button @click="toast" class="button" type="is-default">Toast</b-button>
      <b-button @click="snackbar" class="button" type="is-warning">Snackbar</b-button>
      <b-button @click="dialog" class="button" type="is-info">Dialog</b-button>
    </section>
  </div>
</template>

<script>
  export default {
    name: 'HelloWorld',
    props: {
      msg: String
    },
    methods: {
      toast() {
        this.$toast.open('Something happened')
      },
      snackbar() {
        this.$snackbar.open(`Default, positioned bottom-right with a green 'OK' button`)
      },
      dialog() {
        this.$dialog.alert('Everything looks fine!')
      },
    }
  }
</script>

<style scoped>
  .button {
    margin: 5px;
  }
</style>
