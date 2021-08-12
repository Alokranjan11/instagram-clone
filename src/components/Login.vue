<template>
    <div class="main">
        <div class="login-main">
            <div class="login">
                <img src="img/insta.png" alt="insta-logo"/>
                <h4>{{loginError}}</h4>
                <input v-model="email" type="text" placeholder="Phone number,username or email"/>
                <input v-model="password" type="password" placeholder="Password"/>
                <button @click="login()">Log In</button>
                <p id="login-or">OR</p>
            </div>
            <div class="login-facebook">
                <img src="img/facebook.jpg" alt="facebook-logo"/>
                <h5 id="log">Log in with Facebook</h5>
            </div>
            <div class="login-forgot">
                <p>Forgot Password?</p>
            </div>
        </div>
        <div class="signup">
            <p>Don't have an account?</p>
            <h5 id="sign">Sign up</h5>
        </div>
    </div>
</template>
<script>
export default{
    name:'Instalogin',
    data(){
        return{
            email:"alok@gmail.com",
            password:"12345",
            loginError:"",
        }
    },
    methods:{
        login(){
            if(this.email.includes("@")&&this.password.length>=4){
            this.$router.push("/home")
            }else{
                this.loginError="email and password is incorret"
            }
        }
    }
}
</script>
<style scoped>
.main{
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    margin-top: 20px;
}
.login-main{
    width: 26%;
    height: 20%;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    border: 2px solid #d8d2d2c7;
    margin-top: 30px;
}
.login{
    margin-top: 25px;
    display: flex;
    flex-direction: column;
    justify-content: space-around;
    align-items: center;
}
.login img{
    height: 45%;
    width: 50%;
    margin-bottom: 25px;
}
input{
    height: 35px;
    width: 72%;
    border: 2px solid #d8d2d2c7;
    border-radius: 3px;
    background-color:rgb(248, 248, 248);
    margin: 5px;
    outline: none;
}
button{
    height: 35px;
    width: 75%;
    background-color:#5cb8f5;
    border: none;
    border-radius: 4px;
    color: #fefefe;
    font-size: 16px;
    font-weight: 600;
    margin:13px;
    cursor: pointer;
}
.login-facebook{
    display: flex;
    justify-content: center;
    align-items: center;
    color: rgb(78, 78, 236);
    font-size: 17px;
}
#log{
    cursor: pointer;
}
.login-facebook img{
    width: 10%;
    height: 15%;
    margin: 5px;
    cursor: pointer;
}
.login-forgot{
    color:rgb(78, 78, 236);
    font-size: 13px;
    margin-bottom: 10px;
    cursor: pointer;
}
#login-or{
    color:#beb9b9c7 ;
    font-size: 17px;
    font-weight: 600;
}
.signup{
     width: 26%;
    height: 20%;
    display: flex;
    justify-content: center;
    align-items: center;
    border: 2px solid #d8d2d2c7;
    margin-top: 15px;
}
#sign{
    margin-left: 5px;
    color:#5cb8f5 ;
    font-size: 16px;
    font-weight: 600;
    cursor: pointer;
}
@media screen and (max-width:500px){
    
    .login-main{
        width: 100%;
    }
    .signup{
        width: 100%;
   }
}
@media screen and (min-width:500px) and (max-width:800px){
    
    .login-main{
        width: 60%;
    }
    .signup{
        width: 60%;
   }
}
@media screen and (min-width:800px) and (max-width:1050px){
    
    .login-main{
        width: 50%;
    }
    .signup{
        width: 50%;
   }
}
</style>