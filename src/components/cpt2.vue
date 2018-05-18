<script>
var EmptyList = {template: '<p>Empty list</p>'};  
//当父组件传来的items元素为对象类型时  
var TableList = 'ul'  
// 当父组件定义了isOrdered变量且为true  
var UnorderedList = 'ul'  
export default {
    name:'cpt2',
    functional:true,
    render:function(h,context){
        function getRes(){
            let items=context.props.items;
            if(items.length===0) return EmptyList;
            if (typeof items[0] === 'object') return TableList;  
            //其他  
            return UnorderedList;
        };
        return h(
            getRes(),
            Array.apply(null,{length:context.props.items.length}).map((value,index)=>{
                return h('li',context.props.items[index].name);
            })
        );
    },
    props:{
        items:{
            type:Array,
            required:true
        },
        isOrdered: Boolean
    }
}
</script>
<style scoped>
    li{
        display: inline-block;
        border:1px solid black;
        list-style:none;
    }
</style>
