<template>
  <div
    :id='id'
    @keyup='contentChanged'
    contenteditable="true">{{content}}</div>
</template>

<script>
export default {
  name: 'TextEditable',
  props: {
    value: { type: String, required: true },
    output: { type: String, default: 'text' }
  },
  data () {
    return {
      content: this.value,
      id: Math.random().toString().split('.')[0]
    }
  },
  methods: {
    contentChanged () {
      let el = document.getElementById(this.id)
      this.$emit('input', el.innerHTML)
      /*
      if (this.output === 'html') {
        console.log(el.innerHTML)
        this.$emit('input', el.innerHTML)
      } else {
        this.$emit('input', el.textContent)
      }
      */
    }
  }
}
</script>
