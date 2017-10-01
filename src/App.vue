<template>
  <div id="app">

    <header>
      <img src="./assets/logo.png">
      <a> LOGO </a>
      <p> {{ msg }} </p>
    </header>

    <section class="titlesection">
      <h1> Rewards </h1>
    </section>

    <section>
      <h2> Here is the full list of prizes that you can win. </h2>
      <section class="row1">
        <template v-for="prize in prizes">
          <div class="prizebox">
            <div class="prizeimage">
              <img src="./assets/logo.png">
            </div>
            <h3> {{ prize.prizeName }} </h3>
            <button> Redeem > </button>
          </div>
        </template>
      </section>
    </section>

    <footer>
      <a> Terms & Conditions </a>
      <a> | </a>
      <a> Privacy Policy </a>
    </footer>

  </div>
</template>

<script>
export default {
  name: 'app',
  data () {
    return {
      msg: 'User name here',
      prizes : [
        { prizeName: 'Record Player',
          prizeImage: "./assets/logo.png" },
        { prizeName: 'Smart Phone',
          prizeImage: "./assets/logo.png" },
        { prizeName: 'Concert Tickets',
          prizeImage: "./assets/logo.png" }
      ]
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  margin-top: 60px;
}

h1 {
  font-weight: bold;
}

h2 {
  font-weight: normal;
}


ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}

a {
}

p {
  float: right;
}

.titlesection {
  background-color: blue;
  color: white;
}

.prizebox {
  display: inline-block;
}

footer {
  background-color: black;
  color: white;
}

</style>
