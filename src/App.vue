
<template>
  <CardWrapper>
    <CardHeader />
    <CardMain />
    <CardFooter />
  </CardWrapper>
</template>

<script>
import CardWrapper from './components/CardWrapper.vue';
import CardHeader from './components/CardHeader.vue';
import CardMain from './components/CardMain.vue';
import CardFooter from './components/CardFooter.vue';

export default {
  components: {
    CardWrapper,
    CardHeader,
    CardMain,
    CardFooter,
  }
}
</script>

<style lang="scss">

@import "@/assets/styles/global.scss";
@import "@/assets/styles/base.scss";

</style>
