<template>
  <div id="Metronome">
    <div class="container">
      <div class="metronome">
        <div class="bpm-display">
          <span class="tempo">{{ tempo }}</span>
          <span class="bpm">BPM</span>
        </div>
        <div class="tempo-text">
          <div v-if="this.tempo <= 40">😌</div>
          <div v-if="this.tempo > 40 && this.tempo <= 80">😌</div>
          <div v-if="this.tempo > 80 && this.tempo <= 120">😯</div>
          <div v-if="this.tempo > 120 && this.tempo <= 180">😯</div>
          <div v-if="this.tempo > 180 && this.tempo <= 220">🚀</div>
          <div v-if="this.tempo > 220 && this.tempo <= 240">🚀</div>
          <div v-if="this.tempo > 240 && this.tempo <= 260">🚀</div>
          <div v-if="this.tempo > 260 && this.tempo <= 280">🥱</div>
        </div>
        <div class="tempo-settings">
          <div class="adjust-tempo-btn decrease-tempo" @click="decreaseTempo">
            -
          </div>
          <input
            type="range"
            min="20"
            max="280"
            step="1"
            class="slider"
            v-model.number="tempo"
          />
          <div class="adjust-tempo-btn increase-tempo" @click="increaseTempo">
            +
          </div>
        </div>
        <div class="start-stop" @click="changeStartStop">
          {{ startStopBtn }}
        </div>
        <div class="measures">
          <div class="subtract-beats stepper" @click="decreaseBeat">-</div>
          <div class="measure-count">{{ beat }}</div>
          <div class="add-beats stepper" @click="increaseBeat">+</div>
        </div>
      </div>
    </div>
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
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Raleway:wght@400;700&display=swap");
body {
  font-family: "Raleway", sans-serif;
  color: whitesmoke;
  user-select: none;
  background-color:#4648c9;
}
.container {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 50vh;
}
.metronome {
  display: flex;
  flex-direction: column;
  width: 300px;
  height: 250px;
  justify-content: space-between;
}
.bpm-display {
  width: 100%;
  text-align: center;
  color: #fa545c;
  font-weight: bold;
}
.bpm-display .tempo {
  font-size: 4em;
}
.tempo-text {
  font-size: 0.8em;
  text-transform: uppercase;
  text-align: center;
}
.tempo-text div{
  font-size:30px;
}
.tempo-settings {
  display: flex;
  justify-content: space-between;
}

.tempo-settings .adjust-tempo-btn {
  width: 30px;
  height: 30px;
  font-size: 40px;
  border-radius: 50%;
  border: 1px solid #ddd;
  text-align: center;
  cursor: pointer;
}
.tempo-settings .adjust-tempo-btn:hover {
  background: #fa545c;
  color: #fff;
}
.tempo-settings .decrease-tempo {
  line-height: 25px;
}
.tempo-settings .increase-tempo {
  line-height: 32px;
}

input[type="range"] {
  -webkit-appearance: none;
  background-color: transparent;
  width: 70%;
}
input[type="range"]::-webkit-slider-thumb {
  -webkit-appearance: none;
}
input[type="range"]:focus {
  outline: none;
}

input[type="range"]::-webkit-slider-thumb {
  -webkit-appearance: none;
  width: 16px;
  height: 16px;
  border-radius: 50%;
  background: #fa545c;
  cursor: pointer;
  margin-top: -8px;
}
input[type="range"]::-moz-range-thumb {
  -webkit-appearance: none;
  width: 16px;
  height: 16px;
  border-radius: 50%;
  background: #fa545c;
  cursor: pointer;
  border: none;
}

input[type="range"]::-webkit-slider-runnable-track {
  width: 100%;
  height: 1px;
  background: #ddd;
}

input[type="range"]::-moz-range-track {
  width: 100%;
  height: 1px;
  background: #ddd;
}

.start-stop {
  width: 50px;
  height: 50px;
  font-size: 0.7em;
  text-align: center;
  background: #fa545c;
  border-radius: 50%;
  color: #fff;
  line-height: 50px;
  margin: 0 auto;
  cursor: pointer;
}

.start-stop:hover {
  background: #ff656c;
}
.measures {
  display: flex;
  justify-content: center;
}
.measures .stepper {
  width: 20px;
  height: 20px;
  border-radius: 50%;
  border: 1px solid #ddd;
  text-align: center;
  margin: 0 5px;
  cursor: pointer;
}
.measures .stepper:hover {
  background: #ff656c;
  color: #fff;
}
.measures .add-beats {
  line-height: 20px;
}

.beats-per-measure-text {
  text-align: center;
  font-size: 0.5em;
  text-transform: uppercase;
}

</style>
