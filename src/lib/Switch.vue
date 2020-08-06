<template>
    <button @click="toggle" :class="{checked:value}"><span></span></button>
</template>
<style lang="scss" scoped>
$h:22px;
$h2:$h - 4px;
button{
    width:$h*2;
    height:$h;
    background:grey;
    border:none;
    outline:none;
    border-radius:$h/2;
    position:relative;
    
}
span{
    position: absolute;
    top:2px;
    left:2px;
    width:$h2;
    height:$h2;
    background:white;
    border-radius: $h2/2;
    transition:250ms;
}
button.checked{background:blue;}
button.checked>span{
    left:calc(100% - #{$h2} - 2px);
}
    
</style>
<script lang="ts">
import { ref } from 'vue'
export default {
    props:{
        value:Boolean
    },
    setup(props,context){
        const toggle=(()=>{
          context.emit('update:value',!props.value)
        })
        return {toggle}
    }
}
</script>