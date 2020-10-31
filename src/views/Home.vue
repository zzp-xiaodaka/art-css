<template>
    <div class="home">
        <!-- <img alt="Vue logo" src="../assets/logo.png" /> -->
    </div>
    <layout />
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import Layout from '@/components/layout.vue';

export default defineComponent({
    name: 'Home',
    components: {
        Layout,
    },
});
</script>
