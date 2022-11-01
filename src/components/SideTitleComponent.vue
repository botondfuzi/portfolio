<template>
  <p class="ml-2 text-yellow-300 uppercase tracking-loose" >{{mainTitle}}</p>
  <p class="text-3xl md:text-4xl leading-normal md:leading-relaxed mb-2">{{mainLongTitle}}</p>
  <p class="text-sm md:text-base text-gray-50 mb-4">{{description}}</p>
  <a href="{{btnLink}}"
     class="bg-transparent mr-auto hover:bg-yellow-300 text-yellow-300 hover:text-white rounded shadow hover:shadow-lg py-2 px-4 border border-yellow-300 hover:border-transparent">{{btnLabel}}</a>
</template>

<script>
export default {
  name: "SideTitleComponent",
  props:{
    mainTitle: {
      type: String,
      default:""
    },
    mainLongTitle: {
      type: String,
      default:""
    },
    description: {
      type: String,
      default:""
    },
    btnLabel: {
      type: String,
      default: ""
    },
    btnLink:{
      type:String,
      default: "#"
    }
  },
  setup(){
    return{

    }
  }
}
</script>

<style scoped>

</style>