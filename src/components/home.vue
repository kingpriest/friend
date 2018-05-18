<template>
    <div>
        <p :class="$style.red">
            this must be red
        </p>
        <p :class="[$style.red,$style.bold]">
            this must be red and bold
        </p>
    </div>
</template>
<script>
export default {
    name:'home',
    props:{
        home:String
    },
    created(){
        console.log(this.$style.red);
    }
}
</script>
<style module>
    .red{
        color:red;

    }
    .bold{
        font-weight:bold;
    }
</style>

