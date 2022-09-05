<script setup lang="ts">
import PiKa from "@/assets/img/pika.webp";
import Kabi from "@/assets/img/kabi.webp";
import Keda from "@/assets/img/keda.webp";
import Jieni from "@/assets/img/jieni.webp";

const animalList = [
  {
    id: 1,
    name: "大型仪器A",
    price: "10W",
    unit: "RMB",
    category: "农工院",
    color: "bg-yellow-300",
    description: "实验室",
    img: PiKa
  },
  {
    id: 2,
    name: "大型仪器B",
    price: "20W",
    unit: "RMB",
    category: "计算机学院",
    color: "bg-green-500",
    description: "实验室",
    img: Kabi
  },
  {
    id: 3,
    name: "大型仪器C",
    price: "30W",
    unit: "RMB",
    category: "物联网院",
    color: "bg-yellow-500",
    description: "实验室",
    img: Keda
  },
  {
    id: 4,
    name: "大型仪器D",
    price: "40W",
    unit: "RMB",
    category: "理学院",
    color: "bg-blue-400",
    description: "实验室",
    img: Jieni
  }
];
</script>

<template>
  <el-row>
    <el-col v-for="animal in animalList" :key="animal.id" class="mt-1" :sm="24" :md="12" :xl="6">
      <Panel :banner-color="animal.color" :img-url="animal.img">
        <template #title> {{ animal.name }} </template>
        <template #subtitle> {{ animal.price }} </template>
        <template #badge> {{ animal.unit }} </template>
        <template #banner> {{ animal.category }} </template>
        <template #description> {{ animal.description }} </template>
      </Panel>
    </el-col>
  </el-row>
</template>

<style lang="scss" scoped>
.el-col {
  margin: 8px 0;
}
</style>
