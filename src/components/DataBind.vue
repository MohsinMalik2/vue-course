<template>
    <div>
        <h1>Data Binding</h1>
        <p>Basically it's changing of data in run time like you are enetering any input and its implementing on a data in the body</p>


        <h3>{{message}}</h3>
        <h3 style="white-space:pre-line">{{textarea}}</h3>  <!--For Multiple lines data Like when we use enter inside a text area-->

        <input type="text" v-model="message">
        <textarea type="text" v-model="textarea" />
    </div>
</template>

<script>
export default {
    name:"DataBind",
    data(){
        return {
            message: "Sample Place",
            textarea: "Hi"
        }
    }
}
</script>