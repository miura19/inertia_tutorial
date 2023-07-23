<script setup>
import { Link } from '@inertiajs/vue3';
import { ref } from 'vue';

const newTitle = ref('');
const newContent = ref('');
</script>

<template>
    <div>
        <Link href="/">Link</Link><br>
        <Link :href="route('inertia.index')">名前付きルート</Link><br>
        <Link :href="route('inertia.show', { id: 319 })">パラメーターのテスト</Link><br>

        <div class="mb-8"></div>
        <input type="text" name="newTitle" id="newTitle" v-model="newTitle">{{ newTitle }}<br>
        <input type="text" name="newContent" id="newContent" v-model="newContent">{{ newContent }}<br>
        <Link as="button" :href="route('inertia.store')" method="post" :data="{
            title: newTitle,
            content: newContent
        }">
        DB保存テスト</Link>
    </div>
</template>