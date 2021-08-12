<template>
     <div>
         <div>
             <Header></Header>
         </div>
         <div  class="chat-main">
            <div class="show-chat">
                <div class="name">
                   <p>raj.alok07</p>
                   <img src="img/pencil.png" alt="image"/>
                </div>
                <div class="chat" v-for="data in message" :key="data.id">
                    <img :src="data.image" alt="image"/>
                  <div class="chat-name">
                     <p>{{data.name}}</p>
                     <p id="online">{{data.online}}</p>
                  </div>
                </div>
            </div>
            <div class="message">
                <img src="img/message.png" alt="image"/>
                <p>Your Messages</p>
               <p id="para">Send private photos and messages to a friend or group.</p>
               <button>Send Message</button>
            </div>
         </div>
     </div>
</template>
<script>
import Header from './Header.vue'
export default{
    name:'Chat',
    components:{
        Header,
    },
    data(){
        return{
            message:[
                {id:1,image:"img/alok.jpg",name:"raj.alok07",online:"active 2h ago"},
                {id:2,image:"img/virat.jpeg",name:"yadav23_",online:"active 5h ago"},
                {id:3,image:"img/virat.jpeg",name:"virat.kohli",online:"active 2h ago"},
                {id:4,image:"img/car.jpg",name:"deepakyadav",online:"active 30m ago"},
                {id:5,image:"img/virat.jpeg",name:"ritesh0077",online:"active 5m ago"},
                {id:6,image:"img/virat.jpeg",name:"djyadav70",online:"active 20m ago"},
            ]
        }
    }
}
</script>
<style scoped>
.chat-main{
    display: flex;
    justify-content: space-around;
    align-items: center;
    margin-top: 20px;
    width: 80%;
    border-top: 2px solid rgb(218, 215, 215);
    border-right: 2px solid rgb(218, 215, 215);
    border-bottom: 2px solid rgb(218, 215, 215);
}
.chat{
    display: flex;
    padding: 7px 0px 0px 20px;
    cursor: pointer;
}
.chat img{
    border-radius:50% ;
    height: 70px;
    width: 70px;
}
.name{
    display: flex;
    border-bottom: 2px solid rgb(218, 215, 215);
    align-items: center;
    justify-content: space-around;
  
}
.name p{
    cursor: pointer;
      font-size: 20px;
    font-weight: 500;
}
.name img{
    height: 50px;
    width: 50px;
    border-radius: 50%;
    cursor: pointer;
}
.show-chat{
    border-left: 2px solid rgb(218, 215, 215);
    border-right: 2px solid rgb(218, 215, 215);
    width: 30%;
}
.chat-name{
    margin-left: 10px;
    font-size: 18px;
}
#online{
    margin: -13px 0px 0px 7px;
    font-size: 14px;
}
.message{
    display: flex;
    flex-direction:column ;
    align-items: center;
}
.message img{
    width: 100px;
    height: 100px;
    border: 3px solid black;
    border-radius: 50%;
    padding: 15px;
}
button{
    height: 35px;
    width: 33%;
    border: none;
    border-radius: 3px;
    background-color: #0095f6;
    color: #fefefe;
    font-weight: 550;
    cursor: pointer;
}
.message p{
    font-size: 25px;
}
#para{
    font-size: 15px;
}
@media screen and (max-width:400px){
    .chat-main{
        flex-direction: column;
        border: none;
    }
    .chat-name{
        font-size: 16px;
    } 
    .chat img{
    height: 50px;
    width: 50px;
    }
    .show-chat{
        width: 100%;
    }
    .name{
        border-top: 2px solid rgb(218, 215, 215);
    }
    .message{
        border: 2px solid rgb(218, 215, 215) ;
        width: 100%;
    }
    .message img{
        width: 80px;
        height: 80px;
        margin-top: 20px;
    }
    .message button{
        width: 60%;
        margin-bottom:10px ;
    }
    
}
@media screen and (min-width:400px) and (max-width:600px){
    .chat-main{
        flex-direction: column;
        border: none;
    }
    .chat-name{
        margin-bottom: 20px;
    }
    .show-chat{
        width: 100%;
    }
    .name{
        border-top: 2px solid rgb(218, 215, 215);
    }
    .message{
        border: 2px solid rgb(218, 215, 215) ;
        width: 100%;
    }
    .message img{
        width: 80px;
        height: 80px;
        margin-top: 20px;
    }
    .message button{
        width: 30%;
        margin-bottom:10px ;
    }
    
}
@media screen and (min-width:600px) and (max-width:700px){
    .chat-name{
        margin-bottom: 20px;
    }
    .show-chat{
        width: 70%;
    }
    .message img{
        width: 80px;
        height: 80px;
        margin-top: 20px;
    }
    .message button{
        width: 60%;
        margin-bottom:10px ;
    }
    
}
@media screen and (min-width:700px) and (max-width:800px){
    .show-chat{
        width: 50%;
    }
}
@media screen and (min-width:800px) and (max-width:950px){
    .show-chat{
        width: 40%;
    }
}
</style>