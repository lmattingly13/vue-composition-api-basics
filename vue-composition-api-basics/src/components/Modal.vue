<template>
    <Teleport to=".modal-container">
        <div class="modal">
        <h1>This is a modal</h1>
        <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Nulla possimus similique corporis pariatur, minus a voluptate aspernatur suscipit eligendi repellendus inventore commodi quaerat nisi voluptatum sed magni placeat debitis est.</p>
        <button>Hide Modal</button>
    </div>
    </Teleport>
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