<template>
  <div>
    <div class="fretboard">
      <!-- 一弦 -->
      <div class="string">
        <div class="note-fret">
          <div
            :class="[
              !showE ? 'note-name' : 'note-name-block',
              isShowAllNote ? 'note-name' : 'note-name-block',
            ]"
          >
            E
          </div>
        </div>
        <div class="note-fret">
          <div
            :class="[
              !showF ? 'note-name' : 'note-name-block',
              isShowAllNote ? 'note-name' : 'note-name-block',
            ]"
          >
            F
          </div>
        </div>
        <div class="note-fret">
          <div
            :class="[
              !showGb ? 'note-name' : 'note-name-block',
              isShowAllNote ? 'note-name' : 'note-name-block',
            ]"
          >
            Gb
          </div>
        </div>
        <div class="note-fret">
          <div
            :class="[
              !showG ? 'note-name' : 'note-name-block',
              isShowAllNote ? 'note-name' : 'note-name-block',
            ]"
          >
            G
          </div>
        </div>
        <div class="note-fret">
          <div
            :class="[
              !showAb ? 'note-name' : 'note-name-block',
              isShowAllNote ? 'note-name' : 'note-name-block',
            ]"
          >
            Ab
          </div>
        </div>
        <div class="note-fret">
          <div
            :class="[
              !showA ? 'note-name' : 'note-name-block',
              isShowAllNote ? 'note-name' : 'note-name-block',
            ]"
          >
            A
          </div>
        </div>
        <div class="note-fret">
          <div
            :class="[
              !showBb ? 'note-name' : 'note-name-block',
              isShowAllNote ? 'note-name' : 'note-name-block',
            ]"
          >
            Bb
          </div>
        </div>
        <div class="note-fret">
          <div
            :class="[
              !showB ? 'note-name' : 'note-name-block',
              isShowAllNote ? 'note-name' : 'note-name-block',
            ]"
          >
            B
          </div>
        </div>
        <div class="note-fret">
          <div
            :class="[
              !showC ? 'note-name' : 'note-name-block',
              isShowAllNote ? 'note-name' : 'note-name-block',
            ]"
          >
            C
          </div>
        </div>
        <div class="note-fret">
          <div
            :class="[
              !showDb ? 'note-name' : 'note-name-block',
              isShowAllNote ? 'note-name' : 'note-name-block',
            ]"
          >
            Db
          </div>
        </div>
        <div class="note-fret">
          <div
            :class="[
              !showD ? 'note-name' : 'note-name-block',
              isShowAllNote ? 'note-name' : 'note-name-block',
            ]"
          >
            D
          </div>
        </div>
        <div class="note-fret">
          <div
            :class="[
              !showEb ? 'note-name' : 'note-name-block',
              isShowAllNote ? 'note-name' : 'note-name-block',
            ]"
          >
            Eb
          </div>
        </div>
        <div class="note-fret">
          <div
            :class="[
              !showE ? 'note-name' : 'note-name-block',
              isShowAllNote ? 'note-name' : 'note-name-block',
            ]"
          >
            E
          </div>
        </div>
      </div>
      <!-- 二弦 -->
      <div class="string">
        <div class="note-fret">
          <div
            :class="[
              !showB ? 'note-name' : 'note-name-block',
              isShowAllNote ? 'note-name' : 'note-name-block',
            ]"
          >
            B
          </div>
        </div>
        <div class="note-fret">
          <div
            :class="[
              !showC ? 'note-name' : 'note-name-block',
              isShowAllNote ? 'note-name' : 'note-name-block',
            ]"
          >
            C
          </div>
        </div>
        <div class="note-fret">
          <div
            :class="[
              !showDb ? 'note-name' : 'note-name-block',
              isShowAllNote ? 'note-name' : 'note-name-block',
            ]"
          >
            Db
          </div>
        </div>
        <div class="note-fret">
          <div
            :class="[
              !showD ? 'note-name' : 'note-name-block',
              isShowAllNote ? 'note-name' : 'note-name-block',
            ]"
          >
            D
          </div>
        </div>
        <div class="note-fret">
          <div
            :class="[
              !showEb ? 'note-name' : 'note-name-block',
              isShowAllNote ? 'note-name' : 'note-name-block',
            ]"
          >
            Eb
          </div>
        </div>
        <div class="note-fret">
          <div
            :class="[
              !showE ? 'note-name' : 'note-name-block',
              isShowAllNote ? 'note-name' : 'note-name-block',
            ]"
          >
            E
          </div>
        </div>
        <div class="note-fret">
          <div
            :class="[
              !showF ? 'note-name' : 'note-name-block',
              isShowAllNote ? 'note-name' : 'note-name-block',
            ]"
          >
            F
          </div>
        </div>
        <div class="note-fret">
          <div
            :class="[
              !showGb ? 'note-name' : 'note-name-block',
              isShowAllNote ? 'note-name' : 'note-name-block',
            ]"
          >
            Gb
          </div>
        </div>
        <div class="note-fret">
          <div
            :class="[
              !showG ? 'note-name' : 'note-name-block',
              isShowAllNote ? 'note-name' : 'note-name-block',
            ]"
          >
            G
          </div>
        </div>
        <div class="note-fret">
          <div
            :class="[
              !showAb ? 'note-name' : 'note-name-block',
              isShowAllNote ? 'note-name' : 'note-name-block',
            ]"
          >
            Ab
          </div>
        </div>
        <div class="note-fret">
          <div
            :class="[
              !showA ? 'note-name' : 'note-name-block',
              isShowAllNote ? 'note-name' : 'note-name-block',
            ]"
          >
            A
          </div>
        </div>
        <div class="note-fret">
          <div
            :class="[
              !showBb ? 'note-name' : 'note-name-block',
              isShowAllNote ? 'note-name' : 'note-name-block',
            ]"
          >
            Bb
          </div>
        </div>
        <div class="note-fret">
          <div
            :class="[
              !showB ? 'note-name' : 'note-name-block',
              isShowAllNote ? 'note-name' : 'note-name-block',
            ]"
          >
            B
          </div>
          <div class="double-fretmark"></div>
        </div>
      </div>
      <!-- 三弦 -->
      <div class="string">
        <div class="note-fret">
          <div
            :class="[
              !showG ? 'note-name' : 'note-name-block',
              isShowAllNote ? 'note-name' : 'note-name-block',
            ]"
          >
            G
          </div>
        </div>
        <div class="note-fret">
          <div
            :class="[
              !showAb ? 'note-name' : 'note-name-block',
              isShowAllNote ? 'note-name' : 'note-name-block',
            ]"
          >
            Ab
          </div>
        </div>
        <div class="note-fret">
          <div
            :class="[
              !showA ? 'note-name' : 'note-name-block',
              isShowAllNote ? 'note-name' : 'note-name-block',
            ]"
          >
            A
          </div>
        </div>
        <div class="note-fret">
          <div
            :class="[
              !showBb ? 'note-name' : 'note-name-block',
              isShowAllNote ? 'note-name' : 'note-name-block',
            ]"
          >
            Bb
          </div>
        </div>
        <div class="note-fret">
          <div
            :class="[
              !showB ? 'note-name' : 'note-name-block',
              isShowAllNote ? 'note-name' : 'note-name-block',
            ]"
          >
            B
          </div>
        </div>
        <div class="note-fret">
          <div
            :class="[
              !showC ? 'note-name' : 'note-name-block',
              isShowAllNote ? 'note-name' : 'note-name-block',
            ]"
          >
            C
          </div>
        </div>
        <div class="note-fret">
          <div
            :class="[
              !showDb ? 'note-name' : 'note-name-block',
              isShowAllNote ? 'note-name' : 'note-name-block',
            ]"
          >
            Db
          </div>
        </div>
        <div class="note-fret">
          <div
            :class="[
              !showD ? 'note-name' : 'note-name-block',
              isShowAllNote ? 'note-name' : 'note-name-block',
            ]"
          >
            D
          </div>
        </div>
        <div class="note-fret">
          <div
            :class="[
              !showEb ? 'note-name' : 'note-name-block',
              isShowAllNote ? 'note-name' : 'note-name-block',
            ]"
          >
            Eb
          </div>
        </div>
        <div class="note-fret">
          <div
            :class="[
              !showE ? 'note-name' : 'note-name-block',
              isShowAllNote ? 'note-name' : 'note-name-block',
            ]"
          >
            E
          </div>
        </div>
        <div class="note-fret">
          <div
            :class="[
              !showF ? 'note-name' : 'note-name-block',
              isShowAllNote ? 'note-name' : 'note-name-block',
            ]"
          >
            F
          </div>
        </div>
        <div class="note-fret">
          <div
            :class="[
              !showGb ? 'note-name' : 'note-name-block',
              isShowAllNote ? 'note-name' : 'note-name-block',
            ]"
          >
            Gb
          </div>
        </div>
        <div class="note-fret">
          <div
            :class="[
              !showG ? 'note-name' : 'note-name-block',
              isShowAllNote ? 'note-name' : 'note-name-block',
            ]"
          >
            G
          </div>
        </div>
      </div>
      <!-- 四弦 -->
      <div class="string">
        <div class="note-fret">
          <div
            :class="[
              !showD ? 'note-name' : 'note-name-block',
              isShowAllNote ? 'note-name' : 'note-name-block',
            ]"
          >
            D
          </div>
        </div>
        <div class="note-fret">
          <div
            :class="[
              !showEb ? 'note-name' : 'note-name-block',
              isShowAllNote ? 'note-name' : 'note-name-block',
            ]"
          >
            Eb
          </div>
        </div>
        <div class="note-fret single-fretmark">
          <div
            :class="[
              !showE ? 'note-name' : 'note-name-block',
              isShowAllNote ? 'note-name' : 'note-name-block',
            ]"
          >
            E
          </div>
        </div>
        <div class="note-fret">
          <div
            :class="[
              !showF ? 'note-name' : 'note-name-block',
              isShowAllNote ? 'note-name' : 'note-name-block',
            ]"
          >
            F
          </div>
        </div>
        <div class="note-fret single-fretmark">
          <div
            :class="[
              !showGb ? 'note-name' : 'note-name-block',
              isShowAllNote ? 'note-name' : 'note-name-block',
            ]"
          >
            Gb
          </div>
        </div>
        <div class="note-fret">
          <div
            :class="[
              !showG ? 'note-name' : 'note-name-block',
              isShowAllNote ? 'note-name' : 'note-name-block',
            ]"
          >
            G
          </div>
        </div>
        <div class="note-fret single-fretmark">
          <div
            :class="[
              !showAb ? 'note-name' : 'note-name-block',
              isShowAllNote ? 'note-name' : 'note-name-block',
            ]"
          >
            Ab
          </div>
        </div>
        <div class="note-fret">
          <div
            :class="[
              !showA ? 'note-name' : 'note-name-block',
              isShowAllNote ? 'note-name' : 'note-name-block',
            ]"
          >
            A
          </div>
        </div>
        <div class="note-fret single-fretmark">
          <div
            :class="[
              !showBb ? 'note-name' : 'note-name-block',
              isShowAllNote ? 'note-name' : 'note-name-block',
            ]"
          >
            Bb
          </div>
        </div>
        <div class="note-fret">
          <div
            :class="[
              !showB ? 'note-name' : 'note-name-block',
              isShowAllNote ? 'note-name' : 'note-name-block',
            ]"
          >
            B
          </div>
        </div>
        <div class="note-fret">
          <div
            :class="[
              !showC ? 'note-name' : 'note-name-block',
              isShowAllNote ? 'note-name' : 'note-name-block',
            ]"
          >
            C
          </div>
        </div>
        <div class="note-fret">
          <div
            :class="[
              !showDb ? 'note-name' : 'note-name-block',
              isShowAllNote ? 'note-name' : 'note-name-block',
            ]"
          >
            Db
          </div>
        </div>
        <div class="note-fret">
          <div
            :class="[
              !showD ? 'note-name' : 'note-name-block',
              isShowAllNote ? 'note-name' : 'note-name-block',
            ]"
          >
            D
          </div>
        </div>
      </div>
      <!-- 五弦 -->
      <div class="string">
        <div class="note-fret">
          <div
            :class="[
              !showA ? 'note-name' : 'note-name-block',
              isShowAllNote ? 'note-name' : 'note-name-block',
            ]"
          >
            A
          </div>
        </div>
        <div class="note-fret">
          <div
            :class="[
              !showBb ? 'note-name' : 'note-name-block',
              isShowAllNote ? 'note-name' : 'note-name-block',
            ]"
          >
            Bb
          </div>
        </div>
        <div class="note-fret">
          <div
            :class="[
              !showB ? 'note-name' : 'note-name-block',
              isShowAllNote ? 'note-name' : 'note-name-block',
            ]"
          >
            B
          </div>
        </div>
        <div class="note-fret">
          <div
            :class="[
              !showC ? 'note-name' : 'note-name-block',
              isShowAllNote ? 'note-name' : 'note-name-block',
            ]"
          >
            C
          </div>
        </div>
        <div class="note-fret">
          <div
            :class="[
              !showDb ? 'note-name' : 'note-name-block',
              isShowAllNote ? 'note-name' : 'note-name-block',
            ]"
          >
            Db
          </div>
        </div>
        <div class="note-fret">
          <div
            :class="[
              !showD ? 'note-name' : 'note-name-block',
              isShowAllNote ? 'note-name' : 'note-name-block',
            ]"
          >
            D
          </div>
        </div>
        <div class="note-fret">
          <div
            :class="[
              !showEb ? 'note-name' : 'note-name-block',
              isShowAllNote ? 'note-name' : 'note-name-block',
            ]"
          >
            Eb
          </div>
        </div>
        <div class="note-fret">
          <div
            :class="[
              !showE ? 'note-name' : 'note-name-block',
              isShowAllNote ? 'note-name' : 'note-name-block',
            ]"
          >
            E
          </div>
        </div>
        <div class="note-fret">
          <div
            :class="[
              !showF ? 'note-name' : 'note-name-block',
              isShowAllNote ? 'note-name' : 'note-name-block',
            ]"
          >
            F
          </div>
        </div>
        <div class="note-fret">
          <div
            :class="[
              !showGb ? 'note-name' : 'note-name-block',
              isShowAllNote ? 'note-name' : 'note-name-block',
            ]"
          >
            Gb
          </div>
        </div>
        <div class="note-fret">
          <div
            :class="[
              !showG ? 'note-name' : 'note-name-block',
              isShowAllNote ? 'note-name' : 'note-name-block',
            ]"
          >
            G
          </div>
        </div>
        <div class="note-fret">
          <div
            :class="[
              !showAb ? 'note-name' : 'note-name-block',
              isShowAllNote ? 'note-name' : 'note-name-block',
            ]"
          >
            Ab
          </div>
        </div>
        <div class="note-fret">
          <div
            :class="[
              !showA ? 'note-name' : 'note-name-block',
              isShowAllNote ? 'note-name' : 'note-name-block',
            ]"
          >
            A
          </div>
          <div class="double-fretmark"></div>
        </div>
      </div>
      <!-- 六弦 -->
      <div class="string">
        <div class="note-fret">
          <div
            :class="[
              !showE ? 'note-name' : 'note-name-block',
              isShowAllNote ? 'note-name' : 'note-name-block',
            ]"
          >
            E
          </div>
        </div>
        <div class="note-fret">
          <div
            :class="[
              !showF ? 'note-name' : 'note-name-block',
              isShowAllNote ? 'note-name' : 'note-name-block',
            ]"
          >
            F
          </div>
        </div>
        <div class="note-fret">
          <div
            :class="[
              !showGb ? 'note-name' : 'note-name-block',
              isShowAllNote ? 'note-name' : 'note-name-block',
            ]"
          >
            Gb
          </div>
        </div>
        <div class="note-fret">
          <div
            :class="[
              !showG ? 'note-name' : 'note-name-block',
              isShowAllNote ? 'note-name' : 'note-name-block',
            ]"
          >
            G
          </div>
        </div>
        <div class="note-fret">
          <div
            :class="[
              !showAb ? 'note-name' : 'note-name-block',
              isShowAllNote ? 'note-name' : 'note-name-block',
            ]"
          >
            Ab
          </div>
        </div>
        <div class="note-fret">
          <div
            :class="[
              !showA ? 'note-name' : 'note-name-block',
              isShowAllNote ? 'note-name' : 'note-name-block',
            ]"
          >
            A
          </div>
        </div>
        <div class="note-fret">
          <div
            :class="[
              !showBb ? 'note-name' : 'note-name-block',
              isShowAllNote ? 'note-name' : 'note-name-block',
            ]"
          >
            Bb
          </div>
        </div>
        <div class="note-fret">
          <div
            :class="[
              !showB ? 'note-name' : 'note-name-block',
              isShowAllNote ? 'note-name' : 'note-name-block',
            ]"
          >
            B
          </div>
        </div>
        <div class="note-fret">
          <div
            :class="[
              !showC ? 'note-name' : 'note-name-block',
              isShowAllNote ? 'note-name' : 'note-name-block',
            ]"
          >
            C
          </div>
        </div>
        <div class="note-fret">
          <div
            :class="[
              !showDb ? 'note-name' : 'note-name-block',
              isShowAllNote ? 'note-name' : 'note-name-block',
            ]"
          >
            Db
          </div>
        </div>
        <div class="note-fret">
          <div
            :class="[
              !showD ? 'note-name' : 'note-name-block',
              isShowAllNote ? 'note-name' : 'note-name-block',
            ]"
          >
            D
          </div>
        </div>
        <div class="note-fret">
          <div
            :class="[
              !showEb ? 'note-name' : 'note-name-block',
              isShowAllNote ? 'note-name' : 'note-name-block',
            ]"
          >
            Eb
          </div>
        </div>
        <div class="note-fret">
          <div
            :class="[
              !showE ? 'note-name' : 'note-name-block',
              isShowAllNote ? 'note-name' : 'note-name-block',
            ]"
          >
            E
          </div>
        </div>
      </div>
    </div>
    <div class="note-name-section">
      <ul>
        <li @mouseenter="showC = !showC" @mouseleave="showC = !showC">C</li>
        <li @mouseenter="showDb = !showDb" @mouseleave="showDb = !showDb">
          Db
        </li>
        <li @mouseenter="showD = !showD" @mouseleave="showD = !showD">D</li>
        <li @mouseenter="showEb = !showEb" @mouseleave="showEb = !showEb">
          Eb
        </li>
        <li @mouseenter="showE = !showE" @mouseleave="showE = !showE">E</li>
        <li @mouseenter="showF = !showF" @mouseleave="showF = !showF">F</li>
        <li @mouseenter="showGb = !showGb" @mouseleave="showGb = !showGb">
          Gb
        </li>
        <li @mouseenter="showG = !showG" @mouseleave="showG = !showG">G</li>
        <li @mouseenter="showAb = !showAb" @mouseleave="showAb = !showAb">
          Ab
        </li>
        <li @mouseenter="showA = !showA" @mouseleave="showA = !showA">A</li>
        <li @mouseenter="showBb = !showBb" @mouseleave="showBb = !showBb">
          Bb
        </li>
        <li @mouseenter="showB = !showB" @mouseleave="showB = !showB">B</li>
      </ul>
    </div>
     <!-- 显示所有音符 -->
    <!-- <h2 class="showNoteBtn" @click="isShowAllNote = !isShowAllNote">{{ isShowAllNote ? "显示" : "隐藏" }}所有音符</h2> -->
  </div>
</template>

<script>
export default {
  name: "Guitar",
  data() {
    return {
      isShowAllNote: true,
      showC: false,
      showDb: false,
      showD: false,
      showEb: false,
      showE: false,
      showF: false,
      showGb: false,
      showG: false,
      showAb: false,
      showA: false,
      showBb: false,
      showB: false,
    };
  },
  methods: {},
};
</script>

<style>
@import url("https://fonts.googleapis.com/css?family=Lato:100,300,400");
.showNoteBtn {
  display:flex;
  justify-content:center;
  align-items:center;
  color:aliceblue;
}
.fretboard {
  display: flex;
  flex-direction: column;
  background: #be975b;
  background-image: url(../images/wood-pattern.png);
  width: 100%;
  
  /* height: calc(var(--fretboard-height) * 1px); */
  height: 300px;
  margin-top: 50px;
}
.string {
  width: 100%;
  height: 100%;
  display: flex;
  position: relative;
}

.string:before {
  content: "";
  width: 100%;
  height: 10px;
  background: linear-gradient(#eee, #999);
  box-shadow: 76px 3px 10px #806233;
  z-index: 1;
  position: absolute;
  top: 22px;
  /* top: calc(var(--string-top-position) * 1px); */
}
.note-fret {
  display: flex;
  flex: 1;
  border-right: 10px solid;
  border-image: linear-gradient(to left, #777, #bbb, #777) 1 100%;
  justify-content: center;
  align-items: center;
  position: relative;
}
.note-fret:first-child {
  background: #161717;
  min-width: 76px;
  border-right: 12px solid;
  flex-grow: 0;
  flex-shrink: 0;
  border-image: linear-gradient(to left, #bbb, #fff, #bbb) 1 100%;
}
.note-fret:hover div {
  display: block;
}
.note-name {
  width: 33px;
  height: 33px;
  border-radius: 50%;
  line-height: 33px;
  text-align: center;
  background: teal;
  z-index: 2;
  color: #eee;
  opacity: 100;
  display: none;
}
.note-name-block {
  width: 33px;
  height: 33px;
  border-radius: 50%;
  line-height: 33px;
  text-align: center;
  background: teal;
  z-index: 2;
  color: #eee;
  opacity: 100;
  display: block;
}

.single-fretmark:after,
.double-fretmark:before,
.double-fretmark:after {
  content: "";
  position: absolute;
  height: 20px;
  width: 20px;
  border-radius: 50%;
  background: #806233;
}

.single-fretmark:after {
  top: -1px;
  transform: translate(0, -50%);
}

.double-fretmark:before {
  /* top: calc(var(--double-fretmark-position-1) * 1px); */
  transform: translate(-140%, -50%);
}

.double-fretmark:after {
  /* top: calc(var(--double-fretmark-position-2) * 1px); */
  transform: translate(-140%, -50%);
}
/* 选择音名 */
.note-name-section ul {
  display: flex;
  justify-content: center;
  align-items: center;
  list-style: none;
}
.note-name-section ul li {
  color: black;
  font-weight: 100;
  font-size: 2.5em;
  display: inline;
  margin: 10px;
}
.note-name-section ul>li {
  color:white;
}
.note-name-section li:hover {
  color: #00baba;
}

</style>
