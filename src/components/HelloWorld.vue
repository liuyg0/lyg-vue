<template>
  <div>
    <Row>
      <Button type="primary"  size="default" @click="addEmployee">
        新建
      </Button>
    </Row>
  </div>
</template>

<script>
import axios from 'axios'

export default {
  name: 'HelloWorld',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  },
  methods: {
    addEmployee () {
      console.log('2132123')
      axios.get('http://localhost:8090/hello')
        .then(response => (
          console.log(response.data)
        ))
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>
</style>
