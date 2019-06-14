<template>
  <div id="app">
    <el-button type="primary" @click="openDiag = true">Welcome</el-button>
    <el-dialog :visible.sync="openDiag">
      <div>
        <input type="text" v-model="sendTreat" />
      </div>
      <HelloWorld msg="My first App" />
      <Simba :treat="sendTreat" />
    </el-dialog>
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";
import Simba from "./components/Simba.vue";

export default {
  name: "app",
  components: {
    HelloWorld,
    Simba
  },
  data: function() {
    return {
      sendTreat: "Raw Hide",
      openDiag: false
    };
  }
};
</script>

<style lang="scss">
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
