<template>
  <div class="hello">
    <hr>
    <div id="test" />
  </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from "vue-property-decorator";
import mojs from "@mojs/core";
// import mojs from '@mojs/core';
// import prism from 'prismjs';
// import PrismEditor from 'vue-prism-editor';

@Component
export default class MojsTry extends Vue {
  @Prop() private msg!: string;
  @Prop({
    // type: boolean,
    default: true
  }) private yoyo!: boolean;

  public mounted(): void {
    this.createShape();
    // console.log(this.msg);

    // new mojs.Shape({
    //   parent: '#test',
    //   shape: 'circle',
    //   fill: { '#F64040': '#FC46AD' },
    //   radius: { 20: 80 },
    //   duration: 2000,
    //   isYoyo: true,
    //   isShowStart: true,
    //   easing: 'elastic.inout',
    //   repeat: 1
    // });
  }

  private createShape(): void {
    const bouncyCircle = new mojs.Shape({
      parent: "#test",
      shape: "circle",
      fill: { "#F64040": "#FC46AD" },
      radius: { 20: 80 },
      duration: 2000,
      isYoyo: this.yoyo,
      isShowStart: true,
      easing: "elastic.inout",
      repeat: 1,
    });

    bouncyCircle.play();
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
