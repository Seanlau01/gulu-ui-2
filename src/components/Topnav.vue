<template>
    <div class="topnav clearfix">
        <div class="logo" @click="toggleMenu">LOGO</div>
          <ul class="menu">
              <li>菜单1</li>
              <li>菜单2</li>
          </ul>
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
        padding:16px;  
        position:relative;
        z-index:10;
        display:flex;
        .logo{
            max-width:6em;
          margin-right:auto;
            }
        .menu{
            display: flex;
            flex-wrap:nowrap;
            white-space: nowrap;
            li{
              margin:0 1em;
         }
    }
    
    }
    
    
</style>