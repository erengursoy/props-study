
<template>
  <div>
   
     
     <div  class="container flex justify-center pt-10 ">
       <button
      
        @click="titleDelete()"
          class="block px-5 py-3 text-sm font-medium text-white transition bg-indigo-600 rounded-lg hover:bg-indigo-700 focus:outline-none focus:ring"
          type="button"
        >
        <slot v-if="situation"> </slot>
          <p v-else >{{title}}</p>
        </button>
     </div>
     
    

  </div>
</template>

<script>

export default {
  props:{
  title:{
      type:String,
      required: true,
      default: 'buttons'
    },
   
   
  },
  data: function () {
    return {
      buttonTitle:'',
      
      situation:true,
     
    };
  },
  methods:{
   titleDelete(){
     
   this.$emit('del', this.situation)
   this.situation=!this.situation
 
   
   }

  },
  

  
};
</script>
<style lang='scss'>

</style>
