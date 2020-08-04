<template>
    <div class="topnav clearfix">
        <div class="logo" >LOGO</div>
          <ul class="menu">
              <li>菜单1</li>
              <li>菜单2</li>
          </ul>
          <span class="toggleAside" @click="toggleMenu"></span>
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
        position:fixed;
        top:0;
        left:0;
        width:100%;
        z-index:10;
        display:flex;
        justify-content: center;
        align-items: center;
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
    .toggleAside{
        width:20px;
        height:20px;
        background:red;
        top:50%;
        left:16px;
        transform: translateY(-50%);
        display: none;
        position:absolute;
    }
    @media(max-width:500px){
       .menu{display: none;}
       .logo{margin:0 auto;}
       .toggleAside{display:inline-block;}
    }
    
    }
    
    
</style>