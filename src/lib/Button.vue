<template>
   <button class="gulu-button" :class="`theme-${theme}`">
       <slot/>
   </button>
</template>
<script lang="ts">
export default {
     props:{
       theme:{
         String,
         default:'button'
       }
     }
}
</script>
<style lang="scss" scoped>
 
</style>