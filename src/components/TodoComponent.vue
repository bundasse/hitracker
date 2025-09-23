<script setup>
import { ref } from 'vue';
const editFlg = ref(false);

function setEditFlg(value) {
    editFlg.value = value
}
</script>
<template>
    <div class="d-flex buttons">
      <button v-if="!editFlg" @click="setEditFlg(true)">edit</button>
        <template v-else>
            <button @click="setEditFlg(false)">submit</button>
            <button @click="setEditFlg(false)">cancel</button>
        </template>
    </div>
    <div>
        <ul class="todoList">
            <li class="d-flex">
                <input type="checkbox" name="" id="">
                <p>뭐시기저시기</p>
                <button v-if="editFlg">X</button>
            </li>
        </ul>
    </div>
</template>
<style>
.todoList{
    margin: 0;
    padding: 0;
    list-style: none;
}
</style>