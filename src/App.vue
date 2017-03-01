<template>
  <div id="app">
    <h4>Usage</h4>
    <pre>
      &lt;text-editable v-model='content' &gt;&lt;/text-editable&gt;
    </pre>

    <h4>Example</h4>
    <div>
      <strong>Editable text: (you can edit in place)</strong>
      <text-editable v-model='content' ></text-editable>
      <hr/>
      <strong>Edited text:</strong>
      <p>{{content}}</p>
    </div>
    <!--
    <div>
      <h5>Set <code>output</code> to <code>html</code></h5>
      <strong>Editable text:</strong>
      <text-editable v-model='htmlContent' output='html' ></text-editable>
      <hr/>
      <strong>Edited text:</strong>
      <p v-html='htmlContent'></p>
    </div>
    -->
  </div>
</template>

<script>
import TextEditable from './components/TextEditable'

export default {
  name: 'app',
  components: {
    TextEditable
  },
  data () {
    return {
      content: 'hello world',
      htmlContent: 'hello <b>world</b>'
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
