<template>
  <v-app>
    <v-main>
      <Main></Main>
<!--      <HelloWorld/>-->
    </v-main>
  </v-app>
</template>

<script lang="ts">
import { defineComponent } from 'vue'
import HelloWorld from './components/HelloWorld.vue'
import {invoke} from "@tauri-apps/api/tauri";
import Main from "./pages/Main.vue";

export default defineComponent({
  name: 'App',

  components: {
    Main,
    HelloWorld,
  },

  data () {
    return {
      num : 0,
      name : '1'
    }
  },
    methods: {
      async add() {
        this.num = await invoke("addNum", {num: this.num});
      }
    }
})
</script>
