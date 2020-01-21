<template lang="html">
  <div class="row">
    <label class="custom-label" for="color-select">Цвет:</label>
    <select class="custom-select" v-model="value.color" id="color-select">
      <option value="black">Black</option>
      <option value="red">Red</option>
      <option value="blue">Blue</option>
    </select>

    <label class="custom-label" for="family-select">Шрифт:</label>
    <select class="custom-select" v-model="value.fontFamily" id="family-select">
      <option value="arial">Arial</option>
      <option value="courier">Courier</option>
      <option value="impact">Impact</option>
    </select>

    <label class="custom-label" for="size-select">Размер:</label>
    <select class="custom-select" v-model="value.fontSize" id="size-select">
      <option value="15px">15 px</option>
      <option value="16px">16 px</option>
      <option value="17px">17 px</option>
      <option value="18px">18 px</option>
    </select>
  </div>
</template>

<script>
  export default {
    props: ['value']
  }
</script>

<style lang="css" scoped>
  .row {
    display: flex;
    align-items: center;
    justify-content: space-between;
    margin-bottom: 1rem;
  }

  .custom-label {
    padding: 10px;
    font-size: 16px;
    font-family: Arial;
    color: #495057;
  }

  .custom-label:first-child {
    padding-left: 0;
  }

  .custom-select {
    display: inline-block;
    width: 100%;
    height: calc(1.5em + .75rem + 2px);
    padding: .375rem 1.75rem .375rem .75rem;
    font-size: 1rem;
    font-weight: 400;
    line-height: 1.5;
    color: #495057;
    vertical-align: middle;
    border: 1px solid #ced4da;
    border-radius: .25rem;
    -webkit-appearance: none;
    -moz-appearance: none;
    appearance: none;
    background-image: url("data:image/svg+xml,%3csvg xmlns='http://www.w3.org/2000/svg' width='4' height='5' viewBox='0 0 4 5'%3e%3cpath fill='%23343a40' d='M2 0L0 2h4zm0 5L0 3h4z'/%3e%3c/svg%3e");
    background-repeat: no-repeat;
    background-size: 8px 10px;
    background-position: right .75rem center;
  }

  .custom-select:focus {
    border-color: #80bdff;
    outline: 0;
    box-shadow: 0 0 0 0.2rem rgba(0,123,255,.25);
  }
</style>
