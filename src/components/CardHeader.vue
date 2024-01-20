<template>
    <header>
        <ClipIcon />
        <h1>URL Shortener</h1>
    </header>
</template>

<script>
import ClipIcon from './ClipIcon.vue';

export default {
  components: {
    ClipIcon,
  }
}
</script>

<style>
    header{
        text-align: center;
    }
</style>