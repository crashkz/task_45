<template>
  <div class="block1">
  <form @submit.prevent="inputMessage">
    <center><p>Input data</p></center>
  <input v-model="iMessage1" type="text">
  <input v-model="iMessage2" type="text">
  <input v-model="iMessage3" type="text">
  <input v-model="iMessage4" type="text">
  <input v-model="iMessage5" type="text">

  <div class="btn"><center><button>Save</button></center></div>
</form></div>



</template>

<script>
export default{
  data(){
    return{
      iMessage1: "",
      iMessage2: "",
      iMessage3: "",
      iMessage4: "",
      iMessage5: ""

    }
  },
  methods:{
    inputMessage(){
      this.$emit("newMessage1", this.iMessage1)
      this.$emit("newMessage2", this.iMessage2)
      this.$emit("newMessage3", this.iMessage3)
      this.$emit("newMessage4", this.iMessage4)
      this.$emit("newMessage5", this.iMessage5)
      this.iMessage1 = ""
      this.iMessage2 = ""
      this.iMessage3 = ""
      this.iMessage4 = ""
      this.iMessage5 = ""
    }
  }
}
</script>

<style>
.block1 { 
  width: 175px; 
  background: #9adef7;
  padding: 5px;
  padding-right: 20px; 
  border: solid 2px rgb(87, 200, 252); 
  float: left;
  box-shadow: 0 8px 16px 0 rgba(0,0,0,0.2), 0 6px 20px 0 rgba(0,0,0,0.19);
}

input{
  margin: 10px;
  padding: 10px;
  border: 2px solid rgb(147, 186, 240);
  border-radius: 8px;
}

button{
  width: 50%;
  margin: 10px;
  padding: 10px;
  border: 2px solid rgb(147, 186, 240);
  border-radius: 12px;  
}
</style>
