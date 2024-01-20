<template>
    <div class="input-url">
        <input type="text" :placeholder="placeholder" :disabled="disabled">
        <button class="copy" v-if="showCopyIcon">
            <CopyIcon />
        </button>
    </div>
</template>

<script>
import CopyIcon from './CopyIcon.vue';

export default {
    props: {
        placeholder: String,
        disabled: Boolean,
        showCopyIcon: Boolean
    },
    components: {
        CopyIcon
    }
}
</script>

<style>
    .input-url{
        width: 100%;
        position: relative;
    }
    input{
        border: none;
        text-decoration: none;
        outline: none;
        
        width: 100%;
        border-radius: 4px;
        padding: 0.5rem;
        
        transition: all 0.2s;
        background: var(--purple-light);
        color: var(--white);
        
        transition: all 1s;
        
        &:focus{
            outline: 1px solid var(--purple);
        }
    }
    .copy{
        all: unset;
        position: absolute;
        right: 0;
        top:50%;
        transform: translate(-0.5rem, -50%);
        background: transparent;
    }
</style>