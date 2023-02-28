<script>
export default {
    data(){
        return {
            catName: "",
            catPercent: ''
        }
    },
    emits:['addData'],
    methods: {
        showData() {
            console.log(this.catName)
            console.log(this.catPercent)
        },
        addData(){
            this.$emit('addData', {catName: this.catName, catPercent: this.catPercent})
        }
    }
}
</script>

<template>
  <p style="font-size:30px">add data</p>
  <input type="text" v-model="catName" placeholder="name">
  <input type="number" v-model="catPercent" placeholder="percent">
  <input type="button" value="Add" @click="addData">
</template>

<style>

</style>