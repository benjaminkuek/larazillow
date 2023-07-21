<template>
    <div>Show</div>
    <Link href="/">Main Page</Link>
</template>

<script setup>
    import {Link} from '@inertiajs/vue3'
    defineProps({ message: String })
</script>