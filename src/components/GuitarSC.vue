<template>
  <div class="block">
    <div class="block-name">一个吉他指板音名查看器</div>
    <pre class="block-code" v-highlightjs="code">
    <code>
    </code>
    </pre>
  </div>
</template>

<script>
export default {
  name: "GuitarSC",
  data(){
      return{
          code:`
<template>
<button class="showNoteBtn" @click="isShowAllNote = !isShowAllNote">{{ isShowAllNote ? "显示" : "隐藏" }}所有音符</button>
 <div class="string">
    <div class="note-fret">
        <div :class="[!showE ? 'note-name' : 'note-name-block',isShowAllNote ? 'note-name' : 'note-name-block',]">E</div>
    </div>
    ........
 </div>   
<div class="note-name-section">
    <ul>
        <li @mouseenter="showC = !showC" @mouseleave="showC = !showC">C</li>
     ....
    </ul>
</div>
</template>
<script>
export default {
  name: "Guitar",
  data() {
    return {
      isShowAllNote: true,
      showC: false,
      ....
    };
  },
};
...

 `,
      }
  }
};
</script>

<style>
.block .block-name{
  background-color: #BFCDEB;
  text-align: center;
  font-size: 20px;
  padding-top: 10px;
  border-radius: 10px;
}
.block .block-code{
  background-color: #BFCDEB;
  border-radius: 10px;
}
pre{
    margin: 0px;
}
</style>
