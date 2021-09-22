<template>
  <!-- TODO put these static strings in props -->
  <div class='click-counter-container'>
    <h3>Click Counter Exercise</h3>
    <button id='click_me' type='button' v-on:click='counter++'>Click Me</button>
    <p>You clicked me {{ counter }} times</p>
  </div>
</template>

<script>
export default {
  name: 'ClickCounter',
  data: () => {
    return {
      counter: 0,
    }
  }
}

</script>

<style scoped>
/* Use flexbox in the future */
.click-counter-container {
  border: 1px solid #266DD3;
  margin: 15px auto;
  width: 400px;
  padding: 15px;
}

h3 {
  color: #344055;
}

button {
  padding: 22px 46px;
  font-family: Avenir, Helvetica, Arial, sans-serif;
  text-transform: uppercase;
  font-size: 15px;
  margin: 15px;
  background-color: #266DD3;
  color: #f7f9fc;
  border: 0;
}

</style>