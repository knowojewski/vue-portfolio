<template>
  <div id="app">
    <NavigationMain />
    <router-view/>
  </div>
</template>

<script>
import { Vue, Component } from 'vue-property-decorator';
import NavigationMain from './components/navigation/NavigationMain';

@Component({
  components: {
    NavigationMain
  }
})
export default class App extends Vue {
  
}  
</script>

<style lang="scss">
#app {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
  width: 100%;
}
</style>
