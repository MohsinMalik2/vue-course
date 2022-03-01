<template>
    <div>
        <h1>Props Practice</h1>
        <h2>{{name}}</h2> <!--Single Prop-->
        <h2 v-for="user in users" :key="user.id"> <!--Array Prop-->
            {{user.name}}
        </h2>
    </div>
</template>

<script>
export default ({
  name: "PropsDef",
  props:["name","users"]
})
</script>
