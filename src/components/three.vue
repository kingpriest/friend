
<script>
export default {
  name:'three',
  data(){
      return {
          text:'1234'
      }
  },
  render:function(createElement){
      return createElement('div',
        {//properties&attrs
            class:{
                foo:true
            },
            attrs:{
                id:'foo'
            }
            
        },
        [
            createElement(
                'h1',
                {
                    class:{
                        bar:true
                    },
                    domProps:{
                        innerHTML:'this is h1'
                    }
                }
            )
               
        ]
      );
  }
}
</script>
<style>
    .foo{
        width:300px;
        height: 100px;
        border:1px solid blue;
    }
    .bar{
        background: #ababab;
    }
</style>
