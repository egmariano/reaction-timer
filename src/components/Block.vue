<template lang="">
    <div class="block" v-if="showBlock">
        click me
    </div>
</template>
<script>
export default {
    props: ['delay'],
    data(){
        return {
            showBlock: false
        }
    },
    mounted(){
        console.log('component mounted')
        setTimeout(() => {
            this.showBlock = true
            console.log(this.delay)
        }, this.delay )
    },
}
</script>
<style>
    .block{
        width: 100px;
        border-radius: 20px;
        background: green;
        color: white;
        text-align: center;
        padding: 20px;
        margin: 40px auto;
    }
</style>