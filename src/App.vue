<template>

<MyInput 
  @newMessage1="updateMessage1"
  @newMessage2="updateMessage2"
  @newMessage3="updateMessage3"
  @newMessage4="updateMessage4"
  @newMessage5="updateMessage5"/>

  <div class="block2">
  <MyP :text="message1"/>
  <MyP :text="message2"/>
  <MyP :text="message3"/>
  <MyP :text="message4"/>
  <MyP :text="message5"/>
  </div>


</template>

<script>
// ипорт компонента
import MyP from "@/components/MyP.vue"
import MyInput from "@/components/myInput.vue"

export default{
  // регистрация компонента
  components: {MyP, MyInput},

  data(){
    return{
      message1: "",
      message2: "",
      message3: "",
      message4: "",
      message5: ""

    }
  },
  methods:{
    updateMessage1(eventData){
      this.message1 = eventData
    },
    updateMessage2(eventData){
      this.message2 = eventData
    },
    updateMessage3(eventData){
      this.message3 = eventData
    },
    updateMessage4(eventData){
      this.message4 = eventData
    },
    updateMessage5(eventData){
      this.message5 = eventData
    }
  }
}
</script>

<style>
.block2 { 
  width: 175px; 
  background: #9adef7;
  padding: 5px;
  padding-right: 20px; 
  border: solid 2px rgb(87, 200, 252); 
  float: right;
}
</style>
