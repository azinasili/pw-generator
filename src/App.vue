<template>
<div id="app" class="app">
  <titlebar></titlebar>
  <main class="app-body">
    <pw-content></pw-content>
    <sidebar></sidebar>
  </main>
</div>
</template>

<script>
import Titlebar from './layout/Titlebar';
import PWcontent from './layout/Content';
import Sidebar from './layout/Sidebar';

export default {
  name: 'app',
  components: {
    Titlebar,
    'pw-content': PWcontent,
    Sidebar,
  },
};
</script>

<style lang="scss">
html { box-sizing: border-box; height: 100%; }
*, *::before, *::after { box-sizing: inherit; }
body {
  background: #ff5f6d;
  background: radial-gradient(circle at 65% 100%, #ffc371, #ff5f6d);
  color: rgb(119, 61, 66);
  font-family: 'Source Sans Pro', sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  height: 100%;
  margin: 0;
}

.app {
  display: flex;
  flex-direction: column;
  height: 100vh;
}

.app-body {
  display: flex;
  flex-grow: 1;
  flex-wrap: wrap;
}

.btn {
  border: .0625em solid transparent;
  border-radius: .25em;
  display: inline-block;
  cursor: pointer;
  font-size: 1em;
  font-weight: 400;
  line-height: 1.25;
  padding: .5em 1em;
  text-align: center;
  transition: all .175s ease-in-out;
  user-select: none;
  vertical-align: middle;
  white-space: nowrap;

  .material-icons {
    display: block;
    font-size: 1em;
  }
}

.btn-primary {
  background-color: #0275d8;
  border-color: #0275d8;
  color: #fff;
}

.btn-clear {
  background: none;
  font-size: 1.15em;

  &:hover,
  &:focus {
    background: rgba(255, 255, 255, .26);
  }
}

.btn--fade {
  opacity: .65;

  &:hover,
  &:focus {
    opacity: 1;
  }
}
</style>
