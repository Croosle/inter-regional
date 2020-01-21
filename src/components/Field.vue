<template lang="html">
  <div class="field">
    <div class="row field__row">
      <label class="custom-label" for="color-select">Цвет:</label>
      <select class="custom-select" v-model="selected.color" id="color-select">
        <option value="black">Black</option>
      </select>
      <label class="custom-label" for="family-select">Шрифт:</label>
      <select class="custom-select" v-model="selected.family" id="family-select">
        <option value="arial">Arial</option>
      </select>
      <label class="custom-label" for="size-select">Размер:</label>
      <select class="custom-select" v-model="selected.size" id="size-select">
        <option value="13">13 px</option>
      </select>
    </div>
    <input class="custom-input" v-model="text"/>
  </div>
</template>

<script>
export default {
  data () {
    return {
      selected: {
        color: 'black',
        family: 'arial',
        size: 13
      },
      text: ''
    }
  }
}
</script>

<style lang="css" scoped>
  .row {
    display: flex;
  }

  .field__row {
    align-items: center;
    justify-content: space-between;
    margin-bottom: 1rem;
  }

  .custom-label {
    padding: 10px;
  }

  .custom-input {
    display: block;
    width: 100%;
    padding: .375rem .75rem;
    font-size: 1rem;
    font-weight: 400;
    line-height: 1.5;
    color: #495057;
    background-color: #fff;
    background-clip: padding-box;
    border: 1px solid #ced4da;
    border-radius: .25rem;
    transition: border-color .15s ease-in-out,box-shadow .15s ease-in-out;
  }

  .custom-input:focus {
    color: #495057;
    background-color: #fff;
    border-color: #80bdff;
    outline: 0;
    box-shadow: 0 0 0 0.2rem rgba(0,123,255,.25);
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
  }

  .custom-select:focus {
    border-color: #80bdff;
    outline: 0;
    box-shadow: 0 0 0 0.2rem rgba(0,123,255,.25);
  }
</style>
