<template>
    <div class="modals">
      <h1>Modals</h1>
      <div>
        <label>
            Show Dark Modals?
            <input 
                type="checkbox" 
                v-model="showDarkModals"
                />
        </label>
      </div>
      <button @click="showModal = true">Show modal</button>
      <component 
        v-model="showModal"
        title="My modal(via prop)"
        :is="Modal"
      >
        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Beatae ipsa laboriosam vero natus ut rerum quaerat, saepe praesentium tempore et hic velit odio nemo minus labore quam ullam quod architecto?</p>
      </component>
    </div>
  </template>
  
  <script setup>
  /*
    imports
  */
  
    import { ref } from 'vue'
    import Modal from '@/components/Modal.vue';
  /*
    modals
  */
  
    const showDarkModals = ref(false)
    const showModal = ref(false)
  
  </script>
  