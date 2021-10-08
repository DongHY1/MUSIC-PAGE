<template>
  <div id="app">
    <h1 class="header">🎸 Vue-MusicPage 🎸</h1>
    <Metronome />
    <MetronomeSC/>
    <Guitar />
    <GuitarSC />
    <a href="https://github.com/DongHY1/music-page" class="buttom">➡️ Bring me back to GitHub</a>
  </div>
</template>
<script>
import Metronome from "./components/Metronome.vue";
import Guitar from "./components/Guitar.vue";
import GuitarSC from "./components/GuitarSC.vue"
import MetronomeSC from "./components/MetronomeSC.vue"
export default {
  name: "app",
  components: { Metronome, Guitar,GuitarSC,MetronomeSC},
};
</script>
<style>
*{
  padding:0;
  margin:0;
}
.header {
  display: flex;
  justify-content: center;
  align-items: center;
  margin-top:100px;
  color:aliceblue;
}
.buttom {
  display: flex;
  justify-content: center;
  align-items: center;
  color:aliceblue;
}
a{
  text-decoration: none
}
</style>
