<script setup lang="ts">
import { nextTick, onMounted, ref, watch } from "vue";

const buttons = ["Organize", "Create", "Style", "Share"];
const selectedIndex = ref(0);

const btnBgRefs = ref<HTMLElement[]>([]);
const lastBtnBgRect = ref<DOMRect | null>(null);
const getNewBtnBgRect = () => {
  const btnBgRef = btnBgRefs.value[0];
  return btnBgRef?.getBoundingClientRect();
};

onMounted(() => {
  lastBtnBgRect.value = getNewBtnBgRect();
});

watch(selectedIndex, async () => {
  await nextTick();
  const newBtnBgRect = getNewBtnBgRect();

  if (lastBtnBgRect.value && newBtnBgRect) {
    const btnBgRef = btnBgRefs.value[0];
    btnBgRef.animate(
      [
        {
          transform: `translateX(${
            lastBtnBgRect.value.left - newBtnBgRect.left
          }px)`,
          width: `${lastBtnBgRect.value.width}px`,
          height: `${lastBtnBgRect.value.height}px`,
        },
        {
          transform: `translateX(${0}) translateY(${0})`,
          width: "100%",
          height: "100%",
        },
      ],
      {
        duration: 300,
        easing: "ease",
      }
    );
  }

  lastBtnBgRect.value = newBtnBgRect;
});
</script>

<template>
  <div
    class="relative mx-auto max-w-lg rd-xl bg-black/5 p-1 backdrop-blur-2xl of-hidden"
  >
    <div class="flex flex-row gap-4">
      <div
        v-for="(button, index) in buttons"
        :key="button"
        role="button"
        tabindex="0"
        class="relative basis-1/4 cursor-pointer select-none px-4 py-2"
        @click="selectedIndex = index"
      >
        <div
          class="truncate text-sm font-semibold sm:text-base text-center c-gray-5"
          :class="{ 'c-slate-7': selectedIndex === index }"
        >
          {{ button }}
        </div>
        <div
          ref="btnBgRefs"
          v-if="selectedIndex === index"
          class="absolute inset-0 z-[-1] bg-white rd-[10px] shadow-md hover:shadow-lg"
        ></div>
      </div>
    </div>
  </div>
</template>
