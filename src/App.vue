<template>
  <div>
      <app-header :title="title"></app-header>
      <app-ninjas :ninjas="ninjas"></app-ninjas>
      <app-footer :title="title"></app-footer>
      <app-helper>
        <div slot="form-head">
          <h3>Title of the form</h3>
          <p>info on the form</p>
        </div>
        <div slot="form-fields">
          <input type="text" placeholder="name" required>
          <input type="password" placeholder="password" required>
        </div>
        <div slot="form-controls">
          <button @click="handleSubmit">Submit</button>
        </div>
      </app-helper>
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Footer from './components/Footer.vue'
import Ninjas from './components/Ninjas.vue'
//import formHelper from './components/formHelper.vue'

export default {
  name: 'app',
  data () {
    return {
      ninjas: [
              {name: 'Ryu', speciality: 'Vue Components', show: false},
              {name: 'Crystal', speciality: 'HTML Wizardry', show: false},
              {name: 'Hitoshi', speciality: 'Click Events', show: false},
              {name: 'Tango', speciality: 'Conditionals', show: false},
              {name: 'Kami', speciality: 'Webpack', show: false},
              {name: 'Yoshi', speciality: 'Data Diggin', show: false}
          ],
      title: 'Vue Wizzards'
    }
  },
  components:{
    'app-header': Header,
    'app-footer': Footer,
    'app-ninjas': Ninjas,
    'app-helper': formHelper,
  },
  methods: {
    handleSubmit(){
      alert('submit shot')
    }
    }
  }
</script>

<style scoped>
</style>
