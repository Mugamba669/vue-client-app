<template>
  <div class="home">
    <Input
    @checkNewInput="newInput"
    />
    <button @click="connectServer">Connect</button>
  </div>
</template>

<script>
import Input from "@/components/Input.vue";
export default {
  name: 'Home',
  components: {
   Input,
  },
  methods:{
    connectServer(){
      var socket = new WebSocket("wss://www.nowviba.com/music/index.php");
      socket.onopen =(event)=>{
        console.log(event)
      }
    },
    newInput(value){
        console.log(value);
    }
  }
}
</script>

<style lang="scss" scoped>
      .home{
        display: flex;
        flex-direction: row;
        justify-content: center;
        align-content: center;
        button{
          margin: 10px;
          padding:10px;
          font: 500 18px Ubuntu,Arial;
        }
      }
</style>
