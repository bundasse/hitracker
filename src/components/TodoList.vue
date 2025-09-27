<script setup>
import TodoComponent from '@/components/TodoComponent.vue';

const today= new Date()
const todayYear = today.getFullYear()
const todayMonth = today.getMonth() +1
const todayDate = today.getDate()
</script>
<template>
  <div class="listWrapper">
    <TodoComponent>
      <h2 class="planTitle">
        {{ todayYear }}-{{ todayMonth }}-{{ todayDate }}
      </h2>
    </TodoComponent>
  </div>
</template>

<style>

</style>
