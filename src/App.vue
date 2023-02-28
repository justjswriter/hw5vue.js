<script>
import DiagramData from "./DiagramData.vue"
import Diagram from "./Diagram.vue"
    export default {
        components:{
            DiagramData,
            Diagram
        },
        data() {
            return {
                allData: [
                    {
                        catName: "friends",
                        catPercent: 10
                    },
                    {
                        catName: "hobbies",
                        catPercent: 60
                    },
                    {
                        catName: "study",
                        catPercent: 100
                    }
                ]
            }
        },
        methods: {
            addData(data){
                console.log(data)
                this.allData.push(data)
                console.log(this.allData)
            }
        }

    }
</script>

<template>
    <DiagramData @addData="addData"/>
    <Diagram :allData="allData"/>
</template>

<style scoped>

</style>
