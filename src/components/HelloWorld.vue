<template>
<div class="hello">
  <h1>{{ msg }}</h1>

  <Row>
    <Col span="10" offset="1">
      <router-link to="/grid">grid</router-link>
    </Col>
    <Col span="10" offset="1">col-12</Col>
  </Row>

  <router-view></router-view>
</div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1,
h2 {
  font-weight: normal;
  margin-bottom: 20px;
}

.ivu-col {
  font-size: 16px;
  border: 1px solid #42b983;
}

a {
  color: #42b983;
}
</style>
