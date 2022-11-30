<template>
<div id="app">
    <HeaderBool/>
    <MainBool/>
</div>
</template>

<script>
import MainBool from '@/components/MainBool.vue';
import HeaderBool from '@/components/HeaderBool.vue';

export default {
  name: 'App',
  components: {
    HeaderBool,
    MainBool,
  },
};
</script>

<style lang="scss">
*{
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}
</style>
