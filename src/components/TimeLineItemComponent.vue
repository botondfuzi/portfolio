<template>
  <div class="order-1 w-5/12"></div>
  <div class="order-1 w-5/12 px-1 py-4 text-right">
    <p class="mb-3 text-base text-yellow-300">{{ date }}</p>
    <h4 class="mb-3 font-bold text-lg md:text-2xl">{{ timeLineItemTitle }}</h4>
    <p class="text-sm md:text-base leading-snug text-gray-50 text-opacity-100">
      {{timeLineItemDescription}}
    </p>
  </div>
</template>

<script>
export default {
  name: "TimeLineItemComponent.vue",
  props:{
    date:{
      type:String,
      default: ""
    },
    timeLineItemTitle:{
      type:String,
      default: ""
    },
    timeLineItemDescription:{
      type:String,
      default: ""
    }
  }
}
</script>

<style scoped>

</style>