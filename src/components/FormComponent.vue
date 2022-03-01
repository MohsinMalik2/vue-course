<template>
    <div>
        <h1>Sign up Form</h1>
        <form @submit="signUp">
            <input type="text" placeholder="Username" v-model="signup.username"/><br><br>
            <input type="password" placeholder="Password"  v-model="signup.password"/><br><br>

            <h4>Hobies</h4>
            <input type="checkbox" id="football" value="football" v-model="signup.hobby">
            <label for="football">Football</label>
            <input type="checkbox" id="cricket" value="cricket" v-model="signup.hobby">
            <label for="cricket">Cricket</label>
            <br><br>


            <h4>Gender</h4>

            <input type="radio" id="male" value="male" name="gender" v-model="signup.gender">
            <label for="male">Male</label>
        
            <input type="radio" id="female" value="female" name="gender" v-model="signup.gender">
            <label for="female">Female</label>
            <br><br>

            <button type="submit">Sign Up</button>

        </form>
      


    </div>
</template>
<script>
export default {
    name:"FormComponent",
    data(){
        return {
            signup: {
                username: null,
                password: null,
                hobby: [],
                gender: null,
            }
        }
    },
    methods:{
        signUp(e){
            e.preventDefault();
            if(this.signup.username != null && this.signup.password != null && this.signup.hobby != null && this.signup.gender != null){
                console.log(this.signup)
            }
            else{
                console.warn("Kindly Fill up the fields")
            }
            
        }
    }
}
</script>