<template>
<div class="hello">
  <div class="inputText">
    <form action="http://msg.bar" method="POST">
      <input class="btn striped-shadow dark" type="submit" value="Display">
      <textarea autofocus name="msg" rows="5"
      placeholder="🤘 type
🛰 something
🌐 here
🔐 hit
📡 display" maxlength="72">
      </textarea>
    </form>
  </div>
</div>
</template>

<script>
export default {
  name: 'hello'
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1 {
    color: white;
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
    color: #42b983;
}

textarea {
    border-color: whitesmoke;
    color: whitesmoke;
    background-color: black;
    font-size: 32px;
}

@import 'https://fonts.googleapis.com/css?family=Bungee+Shade';

*,
 :after,
 :before {
    box-sizing: border-box;
}

:focus {
    outline: none;
}

/*div {
    margin: 3rem auto;
    max-width: 660px;
    width: 100%;
    display: flex;
    flex-flow: row wrap;
    justify-content: center;
}*/

button {
    overflow: visible;
    border: 0;
    padding: 0;
    margin: 1.8rem;
}

.btn.striped-shadow span {
    display: block;
    position: relative;
    z-index: 2;
    border: 5px solid;
}

.btn.striped-shadow.dark span {
    border-color: #393939;
    background: #77bfa1;
    color: #FFF;
}

.btn {
    font-family: 'Bungee Shade', sans-serif;
    height: 80px;
    line-height: 65px;
    display: inline-block;
    letter-spacing: 1px;
    position: relative;
    font-size: 1.35rem;
    width: 250px;
    transition: opacity .3s, z-index .3s step-end, -webkit-transform .3s;
    transition: opacity .3s, z-index .3s step-end, transform .3s;
    transition: opacity .3s, z-index .3s step-end, transform .3s, -webkit-transform .3s;
    z-index: 1;
    background-color: transparent;
    cursor: pointer;
    color: white;
}

.btn {
    width: 155px;
    height: 48px;
    line-height: 38px;
}

button.btn.striped-shadow.dark:after,
button.btn.striped-shadow.dark:before {
    background-image: linear-gradient(135deg, transparent 0, transparent 5px, #393939 5px, #393939 10px, transparent 10px);
}

button.btn.striped-shadow:hover:before {
    max-height: calc(100% - 10px);
}

button.btn.striped-shadow:after {
    width: calc(100% - 4px);
    height: 8px;
    left: -10px;
    bottom: -9px;
    background-size: 15px 8px;
    background-repeat: repeat-x;
}

button.btn.striped-shadow:after,
button.btn.striped-shadow:before {
    content: '';
    display: block;
    position: absolute;
    z-index: 1;
    transition: max-height .3s, width .3s, -webkit-transform .3s;
    transition: transform .3s, max-height .3s, width .3s;
    transition: transform .3s, max-height .3s, width .3s, -webkit-transform .3s;
}

.btn.striped-shadow:hover {
    -webkit-transform: translate(-12px, 12px);
    -ms-transform: translate(-12px, 12px);
    transform: translate(-12px, 12px);
    z-index: 3;
}

button.btn.striped-shadow:hover:after,
button.btn.striped-shadow:hover:before {
    -webkit-transform: translate(12px, -12px);
    -ms-transform: translate(12px, -12px);
    transform: translate(12px, -12px);
}

button.btn.striped-shadow:before {
    width: 8px;
    max-height: calc(100% - 5px);
    height: 100%;
    left: -12px;
    bottom: -5px;
    background-size: 8px 15px;
    background-repeat: repeat-y;
    background-position: 0 100%;
}
</style>
