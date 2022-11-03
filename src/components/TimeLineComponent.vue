<template>
  <!-- component -->
  <section>
    <div class="bg-black text-white py-8">
      <div class="container mx-auto flex flex-col items-start md:flex-row my-12 md:my-24">
        <div class="flex flex-col w-full sticky md:top-36 lg:w-1/3 mt-2 md:mt-12 px-8">
          <side-title-component
              :main-title="mainTitle"
              :main-long-title="mainLongTitle"
              :description="description"
              :btn-label="btnLabel"
          />
        </div>
        <div class="ml-0 md:ml-12 lg:w-2/3 sticky">
          <div class="container mx-auto w-full h-full">
            <div class="relative wrap overflow-hidden p-10 h-full">
              <div class="absolute h-full border"
                   style="right: 50%; border: 4px solid #FFC100; border-radius: 5px; background: #FFC100">
              </div>
              <div v-for="item in timeLineItems" :key="item.date" :class="item.position ? 'mb-8 flex justify-between items-center w-full right-timeline':'mb-8 flex justify-between flex-row-reverse items-center w-full left-timeline align-content-start'">
                  <time-line-item-component
                      :date="item.date"
                      :time-line-item-title="item.title"
                      :time-line-item-description="item.description"
                      :side-class="item.position"
                  />
              </div>
            </div>
            <img class="mx-auto -mt-36 md:-mt-36" src="https://user-images.githubusercontent.com/54521023/116968861-ef21a000-acd2-11eb-95ac-a34b5b490265.png" />
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import {ref} from "vue";
import SideTitleComponent from "@/components/SideTitleComponent";
import TimeLineItemComponent from "@/components/TimeLineItemComponent"

export default {
  name: "TimeLineComponent",
  components: {TimeLineItemComponent, SideTitleComponent},
  setup(){
    const mainTitle = ref("My Working Process")
    const mainLongTitle = ref("Hi there! This is me. Botond Füzi")
    const description = ref("Here’s your guide to see my learning process. Go through all the steps to know the where I came from\n")
    const btnLabel = ref("Download CV in english")
    const timeLineItems = [
      {
        date: "2007 - 2015",
        title: "Elementary School",
        institution: {
          name:"Nagy Mózes Elméleti Líceum",
          location: "Romania, Covasna county, Kézdivásárhely"
        },
        description: "Intensive english class",
        position: false
      },
      {
        date: "2015 - 2019",
        title: "High School",
        institution: {
          name:"Nagy Mózes Elméleti Líceum",
          location: "Romania, Covasna county, Kézdivásárhely"
        },
        description: "Natural science with intensive english",
        position: true
      }
    ]

    return{
      mainTitle,
      mainLongTitle,
      description,
      btnLabel,
      timeLineItems
    }
  }
}
</script>

<style scoped>
section{
  font-family: Raleway,sans-serif;
}
</style>