<template>
  <PageTitle page-title='Mayvue Tech Test App'/>
  <MayvueTextbox/>
  <ClickCounter/>
  <div>Thanks for the opportunity to learn VueJS basics in a night</div>
</template>

<script>
import MayvueTextbox from '@/components/Textbox.vue';
import PageTitle from '@/components/PageTitle.vue';
import ClickCounter from '@/components/ClickCounter.vue';

export default {
  name: 'App',
  components: {
    PageTitle,
    MayvueTextbox,
    ClickCounter,
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #262626;
  margin-top: 60px;
}
</style>
