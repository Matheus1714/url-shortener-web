<template>
    <main>
        <InputForm 
            @handleChangeUrl="handleChangeUrl"
            @handleSubmit="handleSubmit"
        />
        <DivLine />
        <OutputDisplay :shortUrl="shortUrl" />
        <DivLine />
    </main>
</template>

<script>
import DivLine from './DivLine.vue';
import InputForm from './InputForm.vue'
import OutputDisplay from './OutputDisplay.vue'

export default {
    components: {
        DivLine,
        InputForm,
        OutputDisplay
    },
    data(){
        return {
            originUrl: "",
            shortUrl: ""
        }
    },
    methods: {
        handleChangeUrl(newUrl){
            this.originUrl = newUrl
        },
        async handleSubmit(){
            try{
                const body = {
                    originURL: this.originUrl
                }
                const response = await fetch(`${API_URL}/shorten`, {
                    method: 'POST',
                    headers: {
                        "Content-Type": "application/json",
                    },
                    body: JSON.stringify(body),
                })
                const data = await response.json()
                this.shortUrl = data['shortURL']
            }catch(error){
                console.log(error)
            }
        }
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