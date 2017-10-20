<template>
    <div>
        <div class="container">
<h1>Testing out this Vue thing.</h1>  

<div class="well">
    <p>Here's some stuff.</p>
    <button type="button" class="btn btn-primary" v-on:click="getQuote()">Push this button</button>
    <p>{{ quote }}</p>
</div>
</div>
</div>
</template>

<script>
export default {
  data () {
    return {
      quote: ''
    }
  },
  methods: {
    qetQuote () {
      console.log('Stuff')
      this.$http
        .get('https://api.chucknorris.io/jokes/random', (data) => {
          this.quote = data
        })
        .error((err) => console.log(err))
    }
  }

}
</script>

<style>
h1 {
    text-align: center;
}
</style>