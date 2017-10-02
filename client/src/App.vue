<template>
  <div id="app">

    <header>
      <img src="./assets/logo.png" class="logoimage">
      <a> LOGO </a>
      <p> Hi, {{ userName }} </p>
    </header>

    <section class="titlesection">
      <h1> Rewards </h1>
    </section>

    <section>
      <h2> Here is the full list of prizes that you can win. </h2>
      <section class="row1">
        <template v-for="prize in prizes">
          <div class="prizebox">
            <div class="prizeimageholder">
              <img v-bind:src = "prize.prizeImage" class="prizeimage">
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
      userName: 'User name here',
      prizes: [
        { prizeName: 'Record Player',
          prizeImage: require('./assets/logo.png') },
        { prizeName: 'Smart Phone',
          prizeImage: require('./assets/logo.png') },
        { prizeName: 'Concert Tickets',
          prizeImage: require('./assets/logo.png') },
        { prizeName: 'Tropical Vacation',
          prizeImage: require('./assets/logo.png') },
        { prizeName: 'Helicopter Tour',
          prizeImage: require('./assets/logo.png') },
        { prizeName: 'New Car',
          prizeImage: require('./assets/logo.png') }
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

.logoimage {
  width: 5%;
}

h1 {
  font-weight: bold;
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
  background-color: rgb(0, 102, 204);
  color: white;
  padding: 60px;
  text-align: center;
}

h2 {
  font-weight: normal;
  text-align: center;
}

.prizebox {
  display: inline-block;
  margin: 2%;
  padding: 15px;
  text-align: center;
  width: 25%;
}

.prizeimageholder {
  width: 100%;
}

.prizeimage {
  width: 100%;
}

footer {
  background-color: black;
  color: white;
  padding: 60px;
  text-align: center;
}

</style>
