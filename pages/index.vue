<template>
<div style="min-height:100vh" class="flex justify-center items-center ">
  <div>
      <ee-card :title="'lorem'" :cardClass="' border border-red-900 '">
       
   <template v-slot:body> 
        <p class="mt-4 text-sm text-gray-300">
    Lorem ipsum dolor sit amet, consectetur adipisicing elit.
  </p>
  </template>
   <template v-slot:footer> 
          <p class="mt-4 text-sm text-gray-300">
    Lorem ipsum dolor sit amet, consectetur adipisicing elit. Odio eius labore nisi tempore modi vel voluptate ullam
    nostrum adipisci suscipit eaque quae cupiditate, accusamus minus laboriosam totam laborum, deserunt sint.
  </p>
  </template>
      </ee-card>
      <ee-button @del="titleFrom" :title="'button'"> 
      <div> hello world</div>
      </ee-button>
      
  </div>
 
  



 
</div>
 
</template>

<script>
import props from '../components/ee-button.vue'
export default {
  components: { props },
  data(){
    return{
      del:'',
    }
  },
  methods: {
    titleFrom(situation){
      this.del=situation
      this.del = !this.del
      console.log(this.del)
    }
  }
  }
</script>
