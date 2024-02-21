<template>
<MainComp></MainComp>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import MainComp from "@/components/MainComp.vue";


export default defineComponent({
  name: 'App',
  components: {MainComp}
});
</script>

<style>

</style>
