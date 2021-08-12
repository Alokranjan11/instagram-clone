<template>
    <div>
        <div class="header">
            <div>
                <img class="insta-logo" src="img/insta.png" alt="instagram-logo"/>
            </div>
            <div>
                <input class="search-bar" type="text" placeholder="search"/> 
            </div>
            <div class="logo">
                    <img @click="homePage" class="logo-size" src="img/home.png" alt="home-logo"/>
                    <img @click="chatPage" class="logo-size" src="img/chat.png" alt="chat-logo"/>
                    <img class="logo-size" src="img/compass.png" alt="compass-logo"/>
                    <img class="logo-size" src="img/like.jpg" alt="like-logo"/>
                    <img @click="profile" class="logo-size" src="img/alok.jpg" alt="profilePhoto-logo"/>
            </div>
        </div>
    </div>
</template>
<script>
export default{
    name:'Header',
    data(){
        return{

        }
    },
    methods:{
        homePage(){
            this.$router.push("/home")
        },
        profile(){
            this.$router.push("/profile")
        },
        chatPage(){
            this.$router.push("/chat")
        }
    }
}
</script>
<style scoped>
.header{
    border-top: 2px solid rgb(209, 202, 202);
    border-bottom: 2px solid rgb(209, 202, 202);
    display: flex;
    justify-content: space-around;
    align-items: center;
}
.insta-logo{
    width: 100%;
    height: 50px;
}
input{
    width: 230px;
    height: 25px;
    text-align: center;
    outline: none;
    border: 2px solid rgb(218, 215, 215);
    border-radius: 3px;
    background-color: rgb(253, 249, 249);
}
.logo{
    display: flex;
}
.logo-size{
    width: 40px;
    height: 35px;
    border-radius: 45%;
    margin: 15px;
    cursor: pointer;
}
@media screen and (max-width: 450px){
    .header{
        width: 100%;
        height: 30%;
        
    }
    .insta-logo{
        width: 80%;
        height: 20px;
    } 
    input{
        width: 50px;
        height: 10px;
        font-size: 5px;
        margin-bottom: 5px;
        margin-right: 5px;
        border: 1px solid rgb(218, 215, 215);
    }
    .logo-size{
        width: 15px;
        height: 15px;
        margin: 3px;
    }
}
@media screen and (min-width: 450px)and (max-width: 750px){
    .header{
        width:100%;
        height: 100%;
        
    }
    .insta-logo{
        width: 60%;
        height: 40px;
    }
    input{
        width: 110px;
        height: 20px;
        font-size: 18px;
        margin-bottom: 5px;
        margin-right: 5px;
        border: 1px solid rgb(218, 215, 215);
    }
    .logo-size{
        width: 30px;
        height: 30px;
        margin: 4px;
    }
}
</style>