<template>
  <input type="text"
    v-model="msg">
</template>


<script>
export default {
 data() {
   return {
     msg:''
   }
 },
 emits:[
   'cm'
 ],
 watch:{
   msg() {
     this.$emit('cm',this.msg)
   }
 }
}
</script>

<style>
  .btn{
    display: inline-block;
    margin:4px;
    padding:6px 12px;
    color: white;
    background: gray;
  }
</style>