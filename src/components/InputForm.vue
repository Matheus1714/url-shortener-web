<template>
    <div class="input-form">
        <CardInput
            placeholder="URL Here"
            :originUrl="originUrl"
            @handleChangeUrl="handleChangeUrl"
        />
        <CardButton
            title="Generate Shortener"
            @click="handleSubmit"
        />
    </div>
</template>

<script>

import CardButton from './CardButton.vue'
import CardInput from './CardInput.vue'

export default {
    components: {
        CardButton,
        CardInput
    },
    data() {
        return {
            originUrl: "",
        }
    },
    methods: {
        handleChangeUrl(newUrl){
            this.$emit('handleChangeUrl', newUrl)
        },
        handleSubmit(){
            this.$emit('handleSubmit')
        }
    }
}
</script>

<style>
.input-form{
    width: 100%;
    display: flex;
    flex-direction: column;
    gap: 1rem;
}
</style>