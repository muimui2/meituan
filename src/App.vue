<template>
  <div id="app">
    <Header />
    <Invite />
    <Menu />
    <Invite />
    <Advertisement />
    <MenuBar />
  </div>
</template>

<script>
import Header from './components/Header'
import Menu from './components/Menu'
import Advertisement from './components/Advertisement'
import Invite from './components/Invite.vue'
import MenuBar from './components/MenuBar.vue'


export default {
  name: 'App',
  components: {
    Header,
    Menu,
    Advertisement,
    Invite,
    MenuBar
  }
}
</script>

<style>
#app {
  padding: 20px 10px;
}
</style>
