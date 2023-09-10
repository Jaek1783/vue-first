<template>
 <!-- counter -->
 <button v-on:click="addNum">+</button>
 <span>{{num}}</span>
 <button v-on:click="minusNum">-</button>    
</template>

<script>
import {ref} from 'vue';
export default{
    setup() {
      const num = ref(1);
      const addNum =  () => {
        ref(num.value = num.value + 1)
        console.log(num.value)
      };
      const minusNum = ()=>{
        ref(num.value = num.value -1)
      }
      return {
        num,
        addNum,
        minusNum
      }
    }
}
</script>