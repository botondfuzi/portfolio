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
                   style="right: 50%; border: 4px solid #FFC100; border-radius: 5px; background: #FFC100"></div>
              <div class="mb-8 flex justify-between flex-row-reverse items-center w-full left-timeline">
                <time-line-item-component
                  :date="dates[0].name"
                  :time-line-item-title="timeLineItemTitles[0].name"
                  :time-line-item-description="timeLineItemDescriptions[0].value"
                />
              </div>
              <div class="mb-8 flex justify-between items-center w-full right-timeline">
                <time-line-item-component
                    :date="dates[0].name"
                    :time-line-item-title="timeLineItemTitles[0].name"
                    :time-line-item-description="timeLineItemDescriptions[0].value"
                />
              </div>
              <div class="mb-8 flex justify-between flex-row-reverse items-center w-full left-timeline">
                <time-line-item-component
                    :date="dates[0].name"
                    :time-line-item-title="timeLineItemTitles[0].name"
                    :time-line-item-description="timeLineItemDescriptions[0].value"
                />
              </div>
              <div class="mb-8 flex justify-between items-center w-full right-timeline">
                <time-line-item-component
                    :date="dates[0].name"
                    :time-line-item-title="timeLineItemTitles[0].name"
                    :time-line-item-description="timeLineItemDescriptions[0].value"
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
    const mainTitle = ref("Working Process")
    const mainLongTitle = ref("Working Process of Fest")
    const description = ref("Here’s your guide to the tech fest 2021 process. Go through all the steps to know the exact process of the\n" +
        "    fest.")
    const btnLabel = ref("Explore Now")
    const dates = [
      {
        name: "1-6 May, 2021"
      }
    ]
    const timeLineItemTitles = [
      {
        name: "Registration"
      }
    ]
    const timeLineItemDescriptions = [
      {
        value: "There was a lot of description, which I deleted, so now I have to write something, because it is it can not be empty."
      }
    ]
    return{
      mainTitle,
      mainLongTitle,
      description,
      btnLabel,
      dates,
      timeLineItemTitles,
      timeLineItemDescriptions
    }
  }
}
</script>

<style scoped>
</style>