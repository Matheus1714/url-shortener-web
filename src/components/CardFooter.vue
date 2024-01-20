<template>
    <a :href="githubURL" target="_blank">
        <GithubIcon />
    </a>
</template>

<script>
import GithubIcon from './GitHubIcon.vue'
export default {
    components: {
        GithubIcon
    },
    data(){
        return {
            githubURL: "https://github.com/Matheus1714/url-shortener-api"
        }
    }
}
</script>

<style lang="scss">
    a {
        display: flex;
        align-items: center;
        justify-content: center;

        border-radius: 9999px;

        transition: all 0.3s;

        &:hover{
            background: var(--purple);
            opacity: 0.8;
        }

        margin-top: auto;
    }
</style>