<template>
  <div class="container">
    <Field/>   
  </div>
</template>

<script>
import Field from './components/Field.vue'

export default {
  name: 'app',
  components: {
    Field
  }
}
</script>

<style>
  .container {
    max-width: 1170px;
    margin: 0px auto;
  }
</style>
