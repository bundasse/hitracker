<script setup>
const today= new Date()
const todayYear = today.getFullYear()
const todayMonth = today.getMonth() +1
const todayDate = today.getDate()
</script>
<template>
  <div>
    <h2>
        {{ todayYear }}-{{ todayMonth }}-{{ todayDate }}
    </h2>
    <ul class="todoList">
        <li class="d-flex">
            <input type="checkbox" name="" id="">
            <p>뭐시기저시기</p>
        </li>
    </ul>
  </div>
</template>

<style>
.d-flex{
    display: flex;
}
</style>
