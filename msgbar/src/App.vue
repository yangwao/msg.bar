<template>
<div id="main">
      <div class="columns">
            <div class="column">
                  <div class="crop">
                        <a href="https://progressbar.sk">
                              <img src="./assets/progressbar-logo.svg" alt="progressbar logo">
                        </a>
                  </div>

            </div>
      </div>
      <div class="columns is-mobile">
            <form action="http://msg.bar" method="POST">
                  <div class="column">
                        <input class="button is-primary is-outlined is-large" type="submit" value="Display" />
                        <a href="https://donate.progressbar.sk">
                              <button class="button is-warning is-outlined is-large">Send 💰⛓ donation</button>
                        </a>
                  </div>
                  <div class="column">
                        <div class="field">
                              <label class="label"></label>
                              <div class="control">
                                    <textarea autofocus name="msg" rows="5" class="textarea" placeholder="🤘 type
🛰 something
🌐 here
🔐 hit
📡 display" maxlength="72">
                                    </textarea>
                              </div>
                        </div>

                  </div>
            </form>
      </div>
</div>
</template>

<script>
export default {
  name: 'app'
}
</script>

<style>
@import "~bulma/css/bulma.css";

html {
    background-color: #000
}

body {}

.textarea {
    border-color: whitesmoke;
    color: whitesmoke;
    background-color: black;
    font-size: 32px;
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
    margin: -128px 0 0 -10px;
}
</style>
