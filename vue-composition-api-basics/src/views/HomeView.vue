
<template>
  <div class = "home">
    <h2>
      {{ appTitle }}
    </h2>

    <h3>{{ counterData.title }}</h3>

    <div>
      <button @click="decreaseCounter(2)" class="btn">--</button>
      <button @click="decreaseCounter(1)" class="btn">-</button>
      <span class="counter">{{ counterData.count }}</span>
      <button @click="increaseCounter(1, $event)" class="btn">+</button>
      <button @click="increaseCounter(2)" class="btn">++</button>
    </div>

    <p>
      This counter is {{ oddOrEvent }}
    </p>

    <div class = "edit">
      <h4> Edit counter title:</h4>
      <input v-model="counterData.title" type="text">
    </div>

    </div>  
</template>

<script setup>
import {reactive, computed, watch} from 'vue'

const appTitle = 'My Ok Counter App'

const counterData = reactive({
  count: 0,
  title: 'My Counter'
})

watch(()=> counterData.count, (newCount)=> {
  if(newCount ===20){
    alert('Way to go! you made it to 20')
  }
  console.log('newCount', newCount)
})

const oddOrEvent = computed(() =>{
  if (counterData.count %2 ===0) return 'even'
  return 'odd'
})
    
const increaseCounter = (amount, e) =>{
  counterData.count += amount
}
const decreaseCounter = amount=>{
  counterData.count -=amount
}

</script>


<style>
.home{
  text-align: center;
  padding: 20px;
}
.btn, .counter{
  font-size: 40px;
  margin:10px;
}
.edit{
  margin-top: 60px;
}
</style>