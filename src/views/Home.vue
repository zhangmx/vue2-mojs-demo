<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js + TypeScript App"/>
    <MojsTry/>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator';
import HelloWorld from '@/components/HelloWorld.vue'; // @ is an alias to /src
import MojsTry from '@/components/MojsTry.vue';

@Component({
  components: {
    HelloWorld,
    MojsTry,
  },
})
export default class Home extends Vue {}
</script>
