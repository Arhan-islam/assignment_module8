<script setup>
import { ref} from 'vue'
import ChildComponent from './ChildComponent.vue';
const person = {
    name:'Ashraful Islam',
    title:'I can ride a Track Marlin 7',
    url:'https://www.trekbikes.com/us/en_US/'
}

const messageToChild = 'Welcome to Child Component'
const messageFromChild = ref('')
</script>
<template>
    <div class="h-screen bg-gradient-to-r flex items-center justify-center flex-col">
        <h1 class="font-bold ">{{ messageFromChild }}</h1>
        <ChildComponent :person = person :messageToChild="messageToChild" v-model:messageFromChild="messageFromChild"></ChildComponent>
    </div>
</template>