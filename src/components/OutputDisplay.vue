<template>
    <div class="output-display">
        <CardInput disabled showCopyIcon :value="shortUrl"/>
        <CardButtonLink title="Go To URL" :shortUrl="shortUrl"/>
    </div>
</template>

<script>
import CardButtonLink from './CardButtonLink.vue'
import CardInput from './CardInput.vue'

export default {
    components: {
        CardInput,
        CardButtonLink
    },
    props: {
        shortUrl: String
    }
}
</script>

<style>
.output-display{
    width: 100%;
    display: flex;
    flex-direction: column;
    gap: 1rem;
}
</style>