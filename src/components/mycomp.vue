<template>
  <div >
      <input type="text" v-haha>
      <p>{{msg}}</p>
      <div v-demo:foo.a.b="abc"></div>
  </div>
</template>
<script>
export default {
    name:'mycomp',
    data(){
        return {
            msg:'',
            message:'hello world',
            text:'',
            abc:'mygoog'
        }
    },
    directives: {
        'haha':{
            inserted:function(el){
                console.log(el);
                el.value='123';
            }
        },
        'demo':{
            bind:function(el,binding,vnode){
                var s = JSON.stringify
                el.innerHTML=
                    'name: '       + s(binding.name) + '<br>' +
                    'value: '      + s(binding.value) + '<br>' +
                    'expression: ' + s(binding.expression) + '<br>' +
                    'argument: '   + s(binding.arg) + '<br>' +
                    'modifiers: '  + s(binding.modifiers) + '<br>' +
                    'vnode keys: ' + Object.keys(vnode).join(', ')
            }
        }     
    }
}
</script>
<style>

</style>
