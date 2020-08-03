<template>
    <div class="topnav clearfix">
        <div class="logo" @click="toggleMenu">LOGO</div>
          <div class="menu" >
          <ul >
              <li>菜单1</li>
              <li>菜单2</li>
          </ul>
          </div>
    </div>
</template>
<script lang="ts">
import { inject, Ref } from 'vue'
    export default {
        setup(){
            const menuVisible=inject<Ref<boolean>>('menuVisible')
            const toggleMenu=()=>{menuVisible.value=!menuVisible.value}
            return {toggleMenu}
        }
    }
</script>
<style lang="scss" scoped>
    .topnav{
        background:#FDC7CB;
        padding:20px;  
        position:relative;
        z-index:10;
    }
    .clearfix::after{
        content:'';
        clear:both;
        display:block;
    }
    .logo{
        float:left;
    }
    ul{
        float:right;
    }
    li{
        float:left;
        margin-left:30px;
    }
    
</style>