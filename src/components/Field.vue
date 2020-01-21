<template lang="html">
  <div class="field">
    <FormattingPanel v-model="styles"/>

    <textarea
      class="custom-textarea"
      placeholder="Введите текст"
      v-model="text"
      :rows="lineCount"
      :style="styles"
    ></textarea>
  </div>
</template>

<script>
import FormattingPanel from './FormattingPanel.vue'

export default {
  components: {
    FormattingPanel
  },
  data () {
    return {
      styles: {
        color: 'black',
        fontFamily: 'arial',
        fontSize: '16px'
      },
      text: ''
    }
  },
  computed: {
    lineCount () {
      const length = this.text.split(/\r\n|\r|\n/).length

      return length < 10 ? length : 10
    }
  }
}
</script>

<style lang="css" scoped>
  .custom-textarea {
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
    resize: none;
    box-sizing: border-box;
  }

  .custom-textarea:focus {
    color: #495057;
    background-color: #fff;
    border-color: #80bdff;
    outline: 0;
    box-shadow: 0 0 0 0.2rem rgba(0,123,255,.25);
  }
</style>
