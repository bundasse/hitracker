<script setup>
import { ref } from 'vue';
const editFlg = ref(false);
const inputValue = ref('')
const addListCount = ref(0)

function setEditFlg(value) {
    editFlg.value = value
    if(!value){
        addListCount.value = 0
    }
}
function setAddList() {
    addListCount.value ++;
}
</script>
<template>
    <div class="d-flex header">
        <slot></slot>
        <div class="d-flex buttons">
            <button v-if="!editFlg" @click="setEditFlg(true)"><i class='bx bx-edit'></i></button>
              <template v-else>
                  <button @click="setAddList()"><i class='bx bx-plus'></i></button>
                  <button @click="setEditFlg(false)"><i class='bx bx-save'></i></button>
                  <button @click="setEditFlg(false)"><i class='bx bx-x'></i></button>
              </template>
        </div>
    </div>
    <div>
        <ul class="todoList">
            <li class="d-flex">
                <input type="checkbox" class="listCheckBox">
                <p class="listText">뭐시기저시기</p>
                <button v-if="editFlg"><i class='bx bx-list-x'></i></button>
            </li>
            <template v-for="num in addListCount" :key="num">
                <li class="d-flex">
                    <input type="checkbox" class="listCheckBox">
                    <input type="text" ref="inputValue">
                </li>
            </template>
        </ul>
    </div>
</template>
<style>
.todoList{
    margin: 12px 0 0;
    padding: 0;
    list-style: none;
}
.todoList>li{
    margin: 0;
    padding: 0;
    align-items: center;
}
.listCheckBox{
    width: 16px;
    height: 16px;
}
button{
    border: 0;
    background: none;
    color: #888888;
    font-size: 20px;
}
button:hover{
    color: black;
}
</style>