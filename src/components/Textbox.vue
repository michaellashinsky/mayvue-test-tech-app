<template>
  <!-- TODO put these static strings in props -->
  <div class='textbox-container'>
    <h3>Textbox Length/Message Exercise</h3>
    <input id='input'
           v-model='text'
           v-on:keyup='keyUp(text)'
           v-bind:class='[textTooLong? tooLongClass : textOKClass]'
           type='text'
           placeholder='Enter some text'/>
    <div class='message-container'>
      <label id='message' class='message'>{{ text }}</label>
    </div>
  </div>
</template>

<script>
export default {
  name: 'MayvueTextbox',
  data: () => {
    return {
      text: '',
      textTooLong: false,
      tooLongClass: 'text-too-long',
      textOKClass: 'text-ok',
    }
  },
  methods: {
    //FIXME scope doesn't allow arrow here...
    keyUp: function (message) {
      this.textTooLong = message.length > 20;
    }
  }
}
</script>

<style scoped>
/* Use flexbox in the future */
.textbox-container {
  border: 1px solid #266DD3;
  height: auto;
  margin: auto;
  width: 400px;
  padding: 15px;
}

h3 {
  color: #344055;
}

input {
  margin: 0 5px;
  border-width: 4px;
}

.message-container {
  margin: 15px;
}

.message {
  overflow-wrap: break-word;
}

input:focus {
  outline: none;
}

.text-ok {
  border-color: #262626;
}

.text-too-long {
  border-color: #ff0000;
}

#message {
  margin: 5px;
}

</style>