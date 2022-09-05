<script lang="ts" setup>
import TopPanel from "./dashboard/TopPanel.vue";
import ActivityCard from "./dashboard/ActivityCard.vue";
import TimeLine from "./dashboard/TimeLine.vue";
import RadarChart from "./dashboard/RadarChart.vue";
import PieChart from "./dashboard/PieChart.vue";
import LineChart from "./dashboard/LineChart.vue";
</script>
<template>
  <!-- Top展示 -->
  <TopPanel />
  <el-row>
    <!-- 隐藏时间线 -->
    <!-- <el-col class="mt-1" :sm="24" :md="6" :xl="6">
      <TimeLine />
    </el-col> -->
    <!-- 排行榜 -->
    <el-col class="mt-1" :sm="24" :md="15" :xl="12">
      <ActivityCard />
    </el-col>
    <!-- 雷达图 -->
    <el-col class="mt-1" :sm="24" :md="9" :xl="6">
      <RadarChart />
    </el-col>
  </el-row>
  <el-row>
    <!-- 折线图 -->
    <el-col class="mt-1" :sm="24" :md="18" :xl="18">
      <LineChart />
    </el-col>
    <!-- 饼图 -->
    <el-col class="mt-1" :sm="24" :md="6" :xl="6">
      <PieChart />
    </el-col>
  </el-row>
</template>

<style scoped></style>
