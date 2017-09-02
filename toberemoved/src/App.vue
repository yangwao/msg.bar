<template>
  <div id="app">
    <!-- <header>
      <span>Led Panel msg.bar</span>
    </header> -->
    <main>
      <div class="crop">
        <a href="https://progressbar.sk"><img src="./assets/progressbar-logo.svg" alt="progressbar logo"></a>
      </div>
      <router-view></router-view>
    </main>
  </div>
</template>

<script>
export default {
  name: 'app'
}
</script>

<style>
body {
  margin: 5px;
  background-color: black;
}

#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #000000;
}

main {
  text-align: center;
  /*margin-top: 0px;*/
}

header {
  margin: 0;
  height: 0px;
  padding: 0 0px 0 0px;
  background-color: #000000;
  color: #ffffff;
}

header span {
  display: block;
  position: relative;
  font-size: 20px;
  line-height: 1;
  letter-spacing: .02em;
  font-weight: 400;
  box-sizing: border-box;
  padding-top: 16px;
}

.crop {
    /*width: 200px;*/
    height: 150px;
    overflow: hidden;
    padding: 10px;
}

.crop img {
    /*width: 400px;*/
    /*height: 300px;*/
    margin: -140px 0 0 -10px;
}
</style>
