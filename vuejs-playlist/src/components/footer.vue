<template>
  <footer>
<p>{{title}}</p>
  </footer>
</template>

<script>
import { bus } from '../main';

export default {
  
  data() {
    return {
        title: '2018'
    }
  },
  created() {
    bus.$on('titleChanged', (data) => {
        this.title = data;
    })
  }
}
</script>

<style scoped>

footer {
  background: #222;
  padding: 6px;
}

p{
  color: lightgreen;
  text-align: center;
}

</style>
