<template>
    <div>
   <Button @click="onClick"
   @focus="onClick"
   @mouseover="onClick">
    我是 Button
   </Button>
    </div>
</template>
<script lang="ts">
import Button from '../lib/Button.vue'
export default {
   components:{ Button },
   setup(){
      const onClick=()=>{

      }
      return {onClick}
   }
}
</script>