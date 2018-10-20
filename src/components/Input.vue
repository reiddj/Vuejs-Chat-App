<template lang="html">
  <div class="Input">
    <div class="form-container">
      <form class="input-form">
        <input type="text" id="input" maxlength="250" name="message" placeholder="Aa" class="message-box">
      </form>
      <button type="submit" name="button" class="send" v-on:keypress="noEnter" v-on:click="submit">Send</button>
    </div>
  </div>
</template>

<script>
export default {
  methods: {
    noEnter: function(e){
      e.preventDefault();
      return e.keycode != 13;
      console.log('Preventing Enter');
    },
    submit: function(e){
      e.preventDefault();
      let mb = document.querySelector('.message-box').value;
      this.validate(mb);
      this.clearInput();
    },
    validate: function(message){
      if(message == ""){
        console.log("You must type in something!")
      }else {
        console.log(message);
        this.generate(message);
      }
    },
    generate: function(mes){
      console.log("Generating the message!");

      let feed = document.getElementById('card-feed');
      let card = document.createElement('div');
      card.id = "card";

      let pic = document.createElement('div');
      pic.id = "profile-pic";

      let name = document.createElement('p');
      name.id = "name";
      name.textContent = "Anon";

      let time = document.createElement('div');
      time.id = "time";
      time.textContent = this.$moment().format('h:mm A');;

      let container = document.createElement('div');
      container.id = "container-u";

      let content = document.createElement('div');
      content.id = "content-box";

      let message = document.createElement('p');
      message.textContent = mes;

      feed.appendChild(card);
      card.appendChild(pic);
      card.appendChild(name);
      card.appendChild(time);
      card.appendChild(container);
      container.appendChild(content);
      content.appendChild(message);
    },
    clearInput: function(){
      let input = document.getElementById('input');
      input.value = "";
    }
  }
}
</script>

<style lang="sass">
  .Input
    position: fixed
    background: #240B3E
    bottom: 0px
    width: 100vw
    height: auto
    min-height: 10vh
    box-shadow: 0px 8px 15px 10px #171717
    margin-top: 30px

  .Input .form-container
    display: flex
    align-items: center
    justify-content: center
    height: 10vh
    //background: red

  .input-form


  input
    background: #19082B
    border: none
    width: 50vw
    font-size: 10px
    min-height: 30px
    height: auto
    word-wrap: break-word
    color: white
    border-radius: 80px
    padding: 0px
    margin-right: 19px
    text-indent: 15px

  input:focus
    box-shadow: 0px 8px 15px #0A0411

  ::placeholder
    color: #BBBBBB

  .send
    width: 40px
    height: 19px
    border: none
    padding: 0px
    background-color: #19082B
    color: white
    border-radius: 20px
    font-size: 10px

  .send:active
    box-shadow: 0px 8px 70px #0A0411
    //color:

</style>
