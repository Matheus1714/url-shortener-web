<template>
    <button>{{ title }}</button>
</template>

<script>
export default {
    props: {
        title: String,
        shortUrl: String
    }
}
</script>

<style lang="scss">
    button{
        border: none;
        text-align: center;
        text-decoration: none;

        background: var(--button-color);
        font-weight: 700;

        width: 100%;
        border-radius: 4px;
        padding: 0.25rem;

        transition: all 0.2s;

        &:hover{
            background: var(--purple-light);
        }
        &:active{
            background: var(--black-light);
        }
    }
</style>
