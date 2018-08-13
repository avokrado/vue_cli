<template>
  <div>
    <form-helper>
    <div slot="form-header">

    </div>
    </form-helper>
  </div>



</template>

<script>
import formHelper from './components/formHelper.vue'
export default {
  components:{
    'form-helper': formHelper
  },
  data() {
    return {
    title: 'Dynamic slot title'
    }
  },
  methods: {
  }
}
</script>

<style>
h2 {
  color:red;
}
</style>
