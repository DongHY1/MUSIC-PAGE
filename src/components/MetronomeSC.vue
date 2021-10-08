<template>
  <div class="block">
    <div class="block-name">一个简易节拍器，可以调整节拍速度和节拍数</div>
    <pre class="block-code" v-highlightjs="code">
    <code></code>
</pre>
  </div>
</template>

<script>
export default {
  name: "MetronomeSC",
  data() {
    return {
      code: `
<template>
  <div id="Metronome">
    <div class="container">
      <div class="metronome">
        <div class="bpm-display">
          <span class="tempo">{{ tempo }}</span>
          <span class="bpm">BPM</span>
        </div>
        <div class="tempo-text">
          <div v-if="this.tempo <= 40">超级慢</div>
          ...
        </div>
        <div class="tempo-settings">
          <div class="adjust-tempo-btn decrease-tempo" @click="decreaseTempo">-</div>
          <input type="range" min="20" max="280" step="1" class="slider" v-model.number="tempo"/>
          <div class="adjust-tempo-btn increase-tempo" @click="increaseTempo">+</div>
        </div>
        <div class="start-stop" @click="changeStartStop">{{ startStopBtn }}</div>
        <div class="measures">
          <div class="subtract-beats stepper" @click="decreaseBeat">-</div>
          <div class="measure-count">{{ beat }}</div>
          <div class="add-beats stepper" @click="increaseBeat">+</div>
        </div>
        <span class="beats-per-measure-text">每小节节拍数</span>
      </div>
    </div>
    <div>一个节拍器，可以调整节拍速度和节拍数</div>
  </div>
</template>
<script>
export default {
  name: "Metronome",
  data() {
    return {
      tempo: 140,
      beat: 4,
      startStopBtn: "开始",
      isRunning: false,
      sounds: {
        strong: new Audio(require("../sound/click1.mp3")),
        weak: new Audio(require("../sound/click2.mp3")),
      },
      code: 'console.log("Hello World")',
      lineNumbers: true
    };
  },
  methods: {
    increaseTempo() {
      if (this.tempo >= 280) return;
      this.tempo++;
    },
    decreaseTempo() {
      if (this.tempo <= 20) return;
      this.tempo--;
    },
    increaseBeat() {
      if (this.beat < 12) {
        this.beat++;
      }
      this.count = 0;
    },
    decreaseBeat() {
      if (this.beat > 2) {
        this.beat--;
      }
      this.count = 0;
    },
    changeStartStop() {
      if (!this.isRunning) {
        this.startStopBtn = "停止";
        this.isRunning = true;
        this.startStrongWeak();
      } else {
        this.startStopBtn = "开始";
        this.isRunning = false;
        this.stopStrongWeak();
      }
    },
    playStrong() {
      this.strong = setTimeout(() => {
        this.sounds.strong.play();
        this.playStrong();
      }, (60000 * this.beat) / this.tempo);
      console.log("strong播放了");
    },
    playWeak() {
      this.weak = setTimeout(() => {
        this.sounds.weak.play();
        this.playWeak();
      }, 60000 / this.tempo);
      console.log("weak播放了");
    },
    startStrongWeak() {
      this.playStrong();
      this.playWeak();
    },
    stopStrongWeak() {
      clearTimeout(this.strong);
      clearTimeout(this.weak);
    },
  },
};
...
            `,
    };
  },
};
</script>

<style>
.block .block-name{
  background-color: #828ff1;
  text-align: center;
  font-size: 20px;
  padding-top: 10px;
  border-radius: 10px;
  color:aliceblue;
  box-shadow: 10px 5px 5px black;
}
.block .block-code{
  background-color: #828ff1;
  border-radius: 10px;
  box-shadow: 10px 5px 5px black;
}
pre{
    margin: 0px;
}
</style>
