<template>
    <div>
        <h1>Currency List</h1>

        <table border="1px">
            <thead>
                <tr>
                    <th>Id</th>
                    <th>Name</th>
                    <th>Symbol</th>
                </tr>
            </thead>
            <tbody>
                <tr v-for="item in list" :key="item.id">
                    <td>{{item.id}}</td>
                    <td>{{item.name}}</td>
                    <td>{{item.symbol}}</td>
                </tr>
            </tbody>
        </table>

    </div>
</template>
<script>
// import Vue from 'vue'
// import VueAxios from 'vue-axios'
import axios from 'axios'
export default {
    name:"CryptocurrencyList",
    data(){
        return {
            list: []
        }
    },
    mounted(){
        axios.get("https://api.coingecko.com/api/v3/coins/markets?vs_currency=usd&order=market_cap_desc&per_page=10&page=1&sparkline=false")
        .then(resp=>{
            return(
                this.list = resp.data,
                console.log(resp.data)
            );
        })
    }
}
</script>