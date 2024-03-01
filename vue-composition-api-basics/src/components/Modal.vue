<template>
    <teleport to=".modal-container">
        <div class="modal">
        <h1><slot name="title"></slot></h1>
        <slot />
        <button>Hide Modal</button>
    </div>
    </teleport>
</template>


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