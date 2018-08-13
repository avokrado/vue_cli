<template>
<header>
<h1 @click="changeTitle"> {{title}}  </h1>
</header>

</template>

<script>
import { bus } from '../main';

export default {
  data() {
    return {
        title: 'Ninja app'
    }
  },
  methods: {
    changeTitle: function() {
      //this.$emit('changeTitle', 'Vue Wizards');
      this.title = 'Vue Avtobus this.title';
      bus.$emit('titleChanged', 'Vue Avtobus');
    }
  }
}
</script>

<style scoped>

header {
  background: red;
  padding: 10px;
}

h1{
  color: #222;
  text-align: center;
}

</style>
