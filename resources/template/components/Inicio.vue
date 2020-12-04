<template>
<nav class="navbar-final">
  <div class="contenedor-buscar">
<div class="primer_multiselect">
  <label class="typo__label">Seccion</label>
  <multiselect v-model="value" :options="options" :custom-label="nameWithLang" placeholder="Select one" label="name" track-by="name"></multiselect>
  <pre class="language-json"><code>{{ value  }}</code></pre>
</div>
  </div>
</nav>
</template>

<script>
import Multiselect from 'vue-multiselect'
export default {
    name: 'inicio',
 components: {
    Multiselect
  },
  data () {
    return {
      value: { name: 'Vue.js', language: 'JavaScript' },
      options: [
        { name: 'Vue.js', language: 'JavaScript' },
        { name: 'Rails', language: 'Ruby' },
        { name: 'Sinatra', language: 'Ruby' },
        { name: 'Laravel', language: 'PHP' },
        { name: 'Phoenix', language: 'Elixir' }
      ]
    }
  },
  methods: {
    nameWithLang ({ name, language }) {
      return `${name} — [${language}]`
    }
  }
}
</script>
<style src="vue-multiselect/dist/vue-multiselect.min.css"></style>
<style scoped>
.primer_multiselect{
  width: 20%;
}

.segundo_multiselect{
  width: 20%;
  right:60%;
}

.contenedor-buscar{
  position: relative;
  top:11px;
}
</style>