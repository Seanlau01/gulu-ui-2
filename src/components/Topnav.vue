<template>
    <div class="topnav clearfix">
        <div class="logo">LOGO</div>
          <div class="menu" >
          <ul >
              <li>菜单1</li>
              <li>菜单2</li>
          </ul>
          </div>
    </div>
</template>
<script lang="ts">
    export default {
        
    }
</script>
<style lang="scss" scoped>
    .topnav{
        background:#FDC7CB;
        padding:20px;  
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