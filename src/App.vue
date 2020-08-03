<template>
   <router-view/>
</template>

<script lang="ts">
import { ref, provide } from 'vue'
export default {
  name: 'App',
  setup(){
      const menuVisiblle=ref(false)
      provide('menuVisible',menuVisiblle)
  }
}
</script>

