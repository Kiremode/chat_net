
<script setup lang="ts">
import UserMsgBox from "./msg_boxes/UserMsgBox.vue";
</script>
<template>
    <div class="chat-holder-window">
        <UserMsgBox>
            <p>Hi</p>
        </UserMsgBox>
        <slot></slot>
    </div>
</template>
<style>
    .chat-holder-window {
        display: flex;
        flex-direction: column;
        padding: 10px;
        background-color: black;
        height:500px;
        overflow-y: auto;
    }
</style>