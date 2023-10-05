<template>
    <div class="msgBox">
        <slot></slot>
    </div>
</template>
<style>
    .msgBox {
        margin-top: 10px;
        display: flex;
        width: 100%;
        color: whitesmoke;
        background-color: #4CAF50;
        border-radius: 5px;
    }
    .msgBox p {
        padding: 10px;
        margin: 0;
    }
</style>