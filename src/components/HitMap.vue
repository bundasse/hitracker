<script setup>
defineProps({
  msg: {
    type: String,
    required: true,
  },
})
function cellColor() {
  return 'lightGray'
}
</script>

<template>
  <div>
    <h1 class="green">To-do MAP</h1>
    <div class="hitMap">
        <template v-for="week in 52" :key="week">
            <template v-for="day in 7" :key="day">
                <div class="cell" :style="'background-color:'+cellColor()"></div>
            </template>
        </template>
    </div>
  </div>
</template>
<style>
.hitMap{
    display: grid;
    grid-template-rows: repeat(7, 1fr);
    grid-template-columns: repeat(52, 1fr);
    gap: 4px;
}
.cell{
    width:16px;
    height:16px;
    border-radius: 2px;
}
</style>
