<template>
    <button @click="toggle" :class="{checked}"><span></span></button>
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
}
button.checked{background:blue;}
button.checked>span{
    left:calc(100% - #{$h2} - 2px);
}
    
</style>
<script lang="ts">
import { ref } from 'vue'
export default {
    setup(){
        const checked=ref(false)
        const toggle=(()=>{
            checked.value=!checked.value
        })
        return {checked,toggle}
    }
}
</script>