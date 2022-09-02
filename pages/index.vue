<template>
  <div>
    <div class="flex justify-center mt-8">
      <div class="w-[800px]">
        <!-- <ButtonBase @click="marginOnRight = !marginOnRight" class="basis-1/6 text-right">Space on Right</ButtonBase> -->
        <div class="
          flex flex-row 
          shadow-lg
          border-gray-300
        ">
          <div class="
          bg-gray-300 
          rounded-l-lg w-8
          flex flex-col text-center divide-y-2 divide-gray-400/25
          ">
            <button @click="marginOnRight = !marginOnRight" class="m-1">
              <ChevronDoubleLeft v-if="!marginOnRight"/>
              <ChevronDoubleRight v-else />
            </button>
          </div>
          <div class="w-full" :class="marginOnRight ? 'mr-96' : ''">
            <textarea
              rows="30"
              name="comment"
              id="comment"
              class="
                block w-full rounded-r-lg sm:text-sm font-mono
                focus:border-0 focus:ring-0
                border-gray-300
                border-l-0
              "
            />
          </div>
        </div>
      </div>
    </div>
    <div>xxx</div>
    <ChevronDoubleRight />
  </div>
</template>

<script setup>
import ArrowLeft from "../components/Icon/ArrowLeft.vue";
import ChevronDoubleLeft from "../components/Icon/ChevronDoubleLeft.vue";
import ChevronDoubleRight from "../components/Icon/ChevronDoubleRight.vue";
  const marginOnRight = ref(false)
</script>