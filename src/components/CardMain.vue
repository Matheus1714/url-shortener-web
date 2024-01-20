<template>
    <main>
        <CardInput placeholder="URL Here"/>
        <CardButton title="Generate Shortener"/>
    
        <DivLine />
    
        <CardInput disabled showCopyIcon/>
        <CardButton title="Go To URL"/>
    
        <DivLine />
    </main>
</template>

<script>
import DivLine from './DivLine.vue';
import CardButton from './CardButton.vue'
import CardInput from './CardInput.vue'

export default {
    components: {
        DivLine,
        CardButton,
        CardInput
    }
}
</script>

<style>
main{
    width: 100%;
    
    margin: 1rem 0;
    display: flex;
    flex-direction: column;
    align-items: center;
    gap: 1rem;
}
</style>