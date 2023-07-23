<script setup>
import { reactive } from 'vue';
import { Inertia } from '@inertiajs/inertia';

const form = reactive({
    title: null,
    content: null
})

const submitFunction = () => {
    Inertia.post('/inertia/store' , form);
}
</script>

<template>
    <div>
        <form @submit.prevent="submitFunction()">
            <input type="text" name="title" v-model="form.title">
            <input type="text" name="content" v-model="form.content">
            <button>送信</button>
        </form>
    </div>
</template>