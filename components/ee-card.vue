
<template>
  <div>
    <div class="container flex justify-center">
      <div class="w-1/3">
        <a
      
          :class="cardClass"
          class="
            block
            p-8
            bg-gray-900
            border border-gray-800
            shadow-xl
            rounded-xl
          "
          href=""
        >
        <div :class="title === undefined ?'hidden': ''" class="text-white " >
          <p class="py-20"  >{{title}}</p>
        </div>
        
         

          <slot name="body"></slot>
          <slot name="footer"></slot>
        </a>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  props: {
    cardClass: "",
    title:undefined,
  },
  data: function () {
    return {};
  },
  methods: {},
};
</script>
<style lang='scss'>
</style>

