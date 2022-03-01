<template>
    <h1 v-if="show"> Hye from Home</h1>
    <h1 v-else> Display when show is false only</h1>
    <h2>{{data}}</h2>
    <h2>{{inte}}</h2>
    <button v-bind:disabled="disableBtn" v-on:click="firstFunction">Call the Function</button>
    <button v-on:click="secFunction">Call the sec Function</button>
    <button v-on:click="display">Call the display Function</button>
    <TableComponent />
    <FooterComponent/>
</template>
<script>

import TableComponent from "./TableComponent.vue";
import FooterComponent from "./FooterComponent.vue";
export default{
    name: "HomeFirst",
    props: {
        data: String,
        inte: Number
    },
     components: {
        TableComponent,
        FooterComponent
    },
    methods:{
        firstFunction()
        {
            console.log("First Function Called");
        },
        secFunction()
        {
            console.log("Sec Function Called");
        },
        display(){
            this.show=!this.show;
        }
    },
    data(){
        return {
            show: true,
            disableBtn: true
        }
    }
   
}
</script>