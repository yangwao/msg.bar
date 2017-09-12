<template>
<div id="main">
      <div class="columns is-mobile">
            <div class="column is-narrow">
                  <div class="crop">
                        <a href="https://progressbar.sk">
                              <img src="./assets/progressbar-logo.svg" alt="progressbar logo">
                        </a>
                  </div>

            </div>
      </div>
      <form action="http://msg.bar" method="POST">
            <div class="columns is-mobile">
                  <div class="column is-narrow">
                        <a href="https://donate.progressbar.sk">
                              <button class="button is-warning is-outlined">Send 💰⛓ donation</button>
                        </a>
                  </div>
                  <div class="column">
                        <input class="button is-primary is-outlined" type="submit" value="Display" />
                  </div>
            </div>
            <div class="columns is-mobile">
                  <div class="column is-narrow">
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
            </div>
            <div class="columns is-mobile">
              <div class="column is-narrow">
                <a @click="getBTCprice()" class="button is-outlined is-warning">Get Bitcoin price</a>
                <a @click="postBTCprice()" class="button is-outlined is-warning">Show Bitcoin price</a>
              </div>
            </div>
      </form>
</div>
</template>

<script>
import axios from 'axios';

export default {
  name: 'app',
  methods: {
    postBTCprice(price) {
      axios({
        method: 'post',
        baseURL: 'http://msg.bar',
        data: {
          msg: this.bitcoinPrice
        }
      })
    },
    getBTCprice() {
      axios({
        method: 'get',
        baseURL: 'https://blockchain.info/ticker'
      })
      .then(response => {
        console.log(response);
        this.bitcoinPrice = response.USD.last
      })
      .catch(e => {
        console.log(e);
      })
    }
  }
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
