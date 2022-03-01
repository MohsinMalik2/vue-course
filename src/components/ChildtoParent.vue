<template>
    <div>
        <h1>Child to Parents</h1>
         <ul>
            <li>
                Make CHild Component
            </li>
            <li>make function on click in child</li>
            <li>In child function use $emit to throw another function like $emit("changeTitle","Parent is Changed")</li>
            <li>In above changeTitle is an emitter to call in parent and other perameter in data</li>
            <li>then in parent call child component and add event with this emiter name</li>
            <li>v-on:changeTitle="changeParentTitle" . In this "changeParentTitle" is another function which'll get child data and replace
                in parent component
            </li>
            
        </ul>

        <button v-on:click="updateTitle">Change Title Now</button>
    </div>
</template>

<script>
export default {
    name: "ChildtoParent",
    methods:{
        updateTitle(){
            this.$emit('changeTitleNow',"Parent is Changed")
        }
    }

}
</script>