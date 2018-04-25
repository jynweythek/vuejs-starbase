<template>
    <div id="app">
        <h3>{{ title }}</h3>
        <div class="row col-md-12">
            <Character v-for="(id, index) in initialIds" :id="id" :key="index"></Character>
        </div>
    </div>
</template>

<script>
  import Character from './components/Character.vue';

  export default {
    name: 'app',
    data() {
      return {
        title: 'Generate your team',
        initialIds: [1, 2, 3]
      }
    },
    components: {
      Character
    }
  }
</script>