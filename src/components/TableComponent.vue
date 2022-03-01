<template>
    <table border="1px">
        <thead>
            <tr>
                <th v-html="htmlChange"></th> <!--Html Binding in Vue-->
                <th>Name</th>
                <th>Email</th>
            </tr>
        </thead>
        <tbody>
            <tr v-for="user in users" :key="user.id"> <!--For Loop in Vue-->
                <td v-bind:style="{color:'red',backgroundColor:'pink'}">{{user.id}}</td> <!--Direct Styling Binding-->
                <td v-bind:class="{blue:show,yellow:!show}">{{user.name}}</td> <!--Class Binding-->
                <td v-bind:class="[show?'yellow':'green']">{{user.email}}</td> <!--Class Binding by array-->
            </tr>
        </tbody>
    </table>
</template>
<script>
export default {
    name: "TableComponent",
    data(){
        return {
            show: false,
            users: [
                {
                    id:1,
                    name: "MOhsin",
                    email: "mohsin@hun.com",
                },
                 {
                    id:2,
                    name: "MOhsin 2",
                    email: "mohsin2@hun.com",
                },
                 {
                    id:3,
                    name: "MOhsin 3",
                    email: "mohsin3@hun.com",
                },
            ],
            htmlChange: "<h5>ID</h5>"
        }
    },
}
</script>
<style scoped>

table{
    text-align: center;
    padding:15px;
    margin: 5px;
    width:100%;
}
.blue{
    color:blue;
}
.yellow{
    color:yellow;
}
.green{
    color:green;
}
</style>