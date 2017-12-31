<template>
  <div>
    <add-blog></add-blog>
  </div>
</template>

<script>
import addBlog from './components/addBlog.vue'

export default {
  name: 'app',
  components: {
    'add-blog': addBlog,
  },
  data () {
    return {

    }
  }
}
</script>

<style scoped>
body{
  margin: 0px;
  font-family: 'Nunito SemiBold';
}
</style>
