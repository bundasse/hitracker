<script setup>
import HitMap from '@/components/HitMap.vue'
import MonthList from '@/components/MonthList.vue';
import TodoList from '@/components/TodoList.vue';
import WeekList from '@/components/WeekList.vue';
</script>

<template>
  <div class="wrapper">
    <HitMap msg="You did it!" />
    <div class="d-flex box" style="border: 1px solid blue">
      <div class="d-flex flex-column">
        <MonthList/>
        <WeekList/>
      </div>
      <TodoList/>
    </div>
  </div>
</template>

<style>
.box{
  justify-content: space-between;
  gap: 12px;
}
.box>div{
  flex-grow: 1;
}
.listWrapper{
  padding: 12px;
  border:1px solid red;
  border-radius: 12px;
}
</style>
