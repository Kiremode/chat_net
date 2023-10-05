<template>
    <div>
        <div class="input-container">
            <input type="text" v-model="message" placeholder="Type your message here...">
            <button @click="sendMessage">Send</button>
        </div>
    </div>
</template>

<script>
export default {
    data() {
        return {
            message: ''
        }
    },
    methods: {
        sendMessage() {
            //make it so that the msg is added in the msgbox and that is added in the chat window
            console.log(this.message)
            const msgBox = document.createElement('div')
            msgBox.classList.add('msgBox')

            if (this.message === '') {
                console.log('empty message please add message')
                return
            }
            const msg = document.createElement('p')
            msg.innerText = this.message

            msgBox.appendChild(msg)

            const chatWindow = document.querySelector('.chat-holder-window')
            chatWindow.appendChild(msgBox)

            this.message = ''
        }
    }
}
</script>

<style scoped>
.input-container {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 10px;
    background-color: #f2f2f2;
    border-radius: 5px;
}

.input-container input {
    flex: 1;
    margin-right: 10px;
    padding: 10px;
    border: none;
    border-radius: 5px;
}

.input-container button {
    background-color: #4CAF50;
    color: white;
    padding: 10px;
    border: none;
    border-radius: 5px;
    cursor: pointer;
}
</style>
