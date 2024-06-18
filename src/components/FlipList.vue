<script lang="ts" setup>
import { nextTick, onMounted, ref, watch } from "vue";

const dataList = ref(Array.from({ length: 100 }, (_, i) => i + 1));
const dataElementRefs = ref<Element[]>([]);
let lastRects = new Map<Element, DOMRect>();

const getNewRects = () => {
  const newRects = new Map<Element, DOMRect>();
  dataElementRefs.value.forEach((element) => {
    newRects.set(element, element.getBoundingClientRect());
  });
  return newRects;
};

onMounted(() => {
  lastRects = getNewRects();
  console.log("lastRects:", lastRects);
});

/** 打乱数组 */
function shuffle<T>(arr: T[]): T[] {
  const copy = arr.slice();
  for (let i = copy.length - 1; i > 0; i--) {
    const j = Math.floor(Math.random() * (i + 1));
    [copy[i], copy[j]] = [copy[j], copy[i]]; // swap
  }
  return copy;
}

/** 翻转数组 */
function reverse<T>(arr: T[]): T[] {
  return arr.slice().reverse();
}

/** 点击按钮时触发 */
function handleReverseBtnClick() {
  dataList.value = reverse(dataList.value);
}

/** 点击按钮时触发 */
function handleShuffleBtnClick() {
  dataList.value = shuffle(dataList.value);
}

watch(dataList, async () => {
  // 等待下一帧，更新元素位置
  await nextTick();
  const newRects = getNewRects();

  lastRects.forEach((lastRect, element) => {
    element.animate(
      [
        {
          transform: `translateX(${
            lastRect.left - newRects.get(element)!.left
          }px) translateY(${lastRect.top - newRects.get(element)!.top}px)`,
        },
        { transform: `translateX(${0}) translateY(${0})` },
      ],
      { duration: 8000, easing: "ease-in-out" }
    );
  });

  lastRects = newRects;
});
</script>

<template>
  <div>
    <div>
      <button @click="handleShuffleBtnClick()">Shuffle</button>
      <button @click="handleReverseBtnClick()">Reverse</button>
    </div>
    <ul class="flip-list">
      <li v-for="item in dataList" :key="item" ref="dataElementRefs">
        {{ item }}
      </li>
    </ul>
  </div>
</template>

<style scoped>
.flip-list {
  list-style: none;
  padding: 0;
  display: grid;
  grid-template-columns: repeat(20, 1fr);
  gap: 8px;
}

.flip-list li {
  width: 50px;
  height: 50px;
  line-height: 50px;
  background-color: white;
  border: 1px solid #ccc;
  border-radius: 12px;
}
</style>
