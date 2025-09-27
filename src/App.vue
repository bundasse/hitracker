<script setup>
import HitMap from '@/components/HitMap.vue'
import MonthList from '@/components/MonthList.vue';
import TodoList from '@/components/TodoList.vue';
import WeekList from '@/components/WeekList.vue';
</script>

<template>
  <div class="wrapper">
    <div class="mainContainer">
      <HitMap msg="You did it!" />
      <div class="d-flex box">
        <div class="d-flex flex-column" style="gap:12px">
          <MonthList/>
          <WeekList/>
        </div>
        <TodoList/>
      </div>
    </div>
  </div>
</template>

<style>
.box{
  justify-content: space-between;
  gap: 12px;
  margin-top: 20px;
}
.box>div{
  flex-grow: 1;
}
.listWrapper{
  padding: 20px;
  border: 1px solid lightblue;
  border-radius: 20px;
}
</style>
