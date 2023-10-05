

<template>
    <div class="chat-holder">
        <slot></slot>
    </div>
</template>

<style>
.chat-holder {
    display: flex;
    flex-direction: column;
    padding: 10px;
    background-color: black;
    overflow-y: auto;
    height:600px;
}
</style>
