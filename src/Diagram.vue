<script>
export default {
  props:['allData']
}
</script>

<template>
<div class="diagram-back">
  <div class="diagram-item" v-for="data in allData" :key="data.index">
    <p class="item-name">{{data.catName}}</p>
    <div  :style="{width: data.catPercent + 'px', height: 7 + 'px', backgroundColor: '#728FCE'}"></div>
  </div>
</div>
</template>

<style>
  p{
    margin: 0;
  }
  .diagram-back{
    background-color: rgb(168, 201, 253);
    width:300px;
    min-height: 100px;
    border: 1px solid rgb(0, 0, 0);
    padding: 20px;
    margin-top: 10px;
  }
  .item-name{
    width: 100px;
  }
  .diagram-item{
    display: flex;
    align-items: center;
  }
</style>