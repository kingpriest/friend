<script>
export default {
    name:'cpt3',
    render:function(h){
        return h(
            'h'+this.level,
            [
                h('a',{
                    attrs:{
                        name:'text',
                        href:'#text'
                    }
                },this.$slots.default)
            ]
        )
    },
    props:{
        level:{
            type:Number,
            required:true
        }
    }
}
</script>
<style>

</style>
