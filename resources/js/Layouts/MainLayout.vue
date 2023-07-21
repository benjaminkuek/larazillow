<template>
  <Link href="/">Main Page</Link>&nbsp; 
  <Link href="/hello">Show Page</Link>
  <div>The page with time {{ timer }}</div> →
  <div v-if="flashSuccess" class="success">
    {{ flashSuccess }}
  </div>
  <slot>Default</slot>
</template>

<script setup>
import {computed} from 'vue'
import { Link, usePage } from '@inertiajs/vue3'
// const x = ref(0)
// const y = computed(() => x.value * 2)
const page = usePage()
const flashSuccess = computed(
  () => usePage().props.flash.success,
)
</script>