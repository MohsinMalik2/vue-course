<template>
  <div>

    <!-- <DataBind/> -->
    <!-- <HomeFirst data="This is  prop data" inte="69"/> -->

 <!-- Pushing single and array prop-->
    <!-- <PropsDef name="Naila" v-bind:users="users" /> -->


<!--Child to Parent Props-->
    <!-- <div>
      <h1>
        {{title}}
      </h1>
        <ChildtoParent v-on:changeTitleNow="newFunction($event)"/>
    </div>-->
  
<!--Child to Parent Props-->

<!--Form Component-->
<FormComponent/>
<!--Form Component-->


<!--API data in Vue-->
<CryptocurrencyList/>
<!--API data in Vue-->

</div> 
</template>

<script>
// import HomeFirst from './components/HomeFirst.vue'
// import DataBind from './components/DataBind.vue'
// import PropsDef from './components/PropsDef.vue'
// import ChildtoParent from './components/ChildtoParent.vue'
// import FormComponent from './components/FormComponent.vue'
import CryptocurrencyList from './components/CryptocurrencyList.vue'
export default {
  name: 'App',
  components: {
    // HomeFirst,
    // DataBind,
    // PropsDef
    // ChildtoParent
    // FormComponent
    CryptocurrencyList

  },
  data(){
    return{
        users: [
          {
            name: "King",
            id:1
          },
          {
            name: "Queen",
            id:2
          },
          {
            name: "Jack",
            id:3
          },
          {
            name: "Ace",
            id:4
          },
        ],
        title:"Old Title"

    }
  },
  methods:{
    newFunction(title){
      // alert(title);
      this.title = title;
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
