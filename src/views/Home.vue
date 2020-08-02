<template>
    <div>
        <Topnav/>
      <div class="banner">
        <h1>咕噜UI</h1>
        <h2>一个厉害的UI框架</h2>
        <p class="actions">
           <a href="https://github.com">GitHub</a>
           <router-link to="/doc">开始</router-link>
        </p>
      </div>
    </div>
</template>

<script lang="ts">
import Topnav from '../components/Topnav.vue'
export default {
    components:{Topnav}
}
</script>

<style lang="scss" scoped>
.banner{
   background:#89DF8D;
   padding:100px 0;
   display:flex;
   justify-content: center;
   align-items:center;
   flex-direction:column;
   .actions{
     padding:8px 0; 
   }
    a{
        background:white;
        border-radius:8px;
        padding:3px 5px;
        margin:0 8px;
        display:inline-block;
        $h:28px;
        height:$h;
        line-height:$h;
        border-radius:$h/2;
        padding:0 8px;
    }
}
</style>
    