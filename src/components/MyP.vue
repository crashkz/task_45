<template>
    <p>
      Data {{ text }}
    </p>
  </template>
  
<script>
  
export default{
        props:{
            text:{
                type: String,
                required: true
            }
        }
}
</script>
  
<style>
p{
  margin: 10px;
  padding: 10px;
  border: 2px solid rgb(147, 186, 240);
  border-radius: 4px;
}
</style>
  