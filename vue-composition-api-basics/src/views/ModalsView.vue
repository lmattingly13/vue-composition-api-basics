<template>
    <div class="modals">
        <h1> Modals</h1>
        <button @click="showModal=true">Show Modal</button>
        <Teleport to=".modal-container">
            <div 
            v-if = "showModal" 
            class="modal"
            >
            <h1>This is a modal</h1>
            <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Nulla possimus similique corporis pariatur, minus a voluptate aspernatur suscipit eligendi repellendus inventore commodi quaerat nisi voluptatum sed magni placeat debitis est.</p>
            <button @click="showModal=false">Hide Modal</button>
        </div>
        </Teleport>
    </div>
</template>

<script setup>
import {ref} from 'vue'
/*modals*/

const showModal = ref(false)
</script>

<style>
.modal{
    background:beige;
    padding:10px;
    position:absolute;
    left: 0;
    top:0;
    width: 100%;
    height: 100%;
    z-index: 1;
}

</style>