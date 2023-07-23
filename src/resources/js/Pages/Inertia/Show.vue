<script setup>
import { Link } from '@inertiajs/vue3';
defineProps({
    id : String
})
</script>

<template>
    <div>
        <h1>Show</h1>
        {{ id }}
    </div>
</template>