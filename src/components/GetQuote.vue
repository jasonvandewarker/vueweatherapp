<template>
  <div>
        
    <h1>Testing out this Vue thing.</h1>
      <div class="ui card">
          <p>Here's some stuff.</p>
          <button type="button" class="btn btn-primary" v-on:click="getQuote()">Push this button</button>
          <p>This is where the quote will go {{ quote }}</p>
      </div>

  </div>
</template>

<script>
export default {
  data() {
    return {
      quote: ''
    }
  },
  methods: {
    qetQuote () {
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