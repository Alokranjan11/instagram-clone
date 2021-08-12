<template>
    <div>
        <div>
            <Header></Header>
        </div>
       <div> 
        <div class="profile">
            <div class="profile-img">
                <img src="img/alok.jpg" alt="profile-photo"/>
            </div>
            <div class="profile-deatils">
                <div class="profile-edit">
                   <p>raj.alok07</p>
                   <button>Edit Profile</button>
                   <img src="img/setting.jpg" alt="setting"/>
                </div>
                <div class="friend">
                    <p>0 post</p>
                    <p>200 Followers</p>
                    <p>150 Follwing </p>
                </div>
                <div class="name">
                    <p>Alok Yadav</p>
                </div>
            </div>
        </div>
          <div class="post-main">
             <div class="post-img">
                <div v-for="data in img" :key="data.id">
                    <img :src="data.image" alt="image"/>
                 </div>
             </div>
          </div>
       </div> 
    </div>
</template>
<script>
import Header from './Header.vue'
export default{
    name:'Profile',
    // props:['newData'],
    components:{
        Header,
    },
    data(){
        return{
            img:[
                {id:1,image:"/img/alok.jpg"},
                {id:2,image:"/img/virat.jpeg"},
                {id:3,image:"/img/jeep.jpg"},
                {id:4,image:"/img/profilephoto.jpeg"},
                {id:5,image:"img/car.jpg"},
                {id:6,image:"img/insta.png"},
            ]
        }
    }
}
</script>
<style scoped>
.profile{
    display: flex;
    justify-content: center;
    align-items: center;
}
.profile-deatils{
    margin-left:7% ;
}
.profile-edit{
    display: flex;
    align-items: center;
    font-size: 30px;
}
button{
    border: 2px solid rgb(199, 196, 196);
    border-radius: 3px;
    height: 35px;
    width: 100px;
    font-size: 14px;
    font-weight: 600;
    background-color: #fefefe;
    margin-left: 15px ;
    cursor: pointer;
}
.friend{
    display: flex;
    justify-content: space-between;
    align-items: center;
    font-size: 18px;
    cursor: pointer;
}
.profile-img img{
    height: 220px;
    width: 220px;
    border-radius: 50%;
    cursor: pointer;
}
.profile-edit img{
    height: 40px;
    width: 45px;
    cursor: pointer;
    margin-left: 15px;
}
.name{
    text-align: left;
    font-size: 23px;
}
.post-main{
    display: flex;
    justify-content: center;
}
.post-img{
    width: 50%;
    display: flex;
    justify-content: center;
    flex-wrap: wrap;
    margin-top: 20px;
    border-top: 2px solid rgb(214, 210, 210);

}
.post-img img{
    height: 200px;
    width: 200px;
    margin-top: 20px;
}
@media screen and (max-width:350px) {
     .post-img img{
        height: 80px;
        width: 80px;
    }
    .profile-img img{
    height: 95px;
    width: 90px;
    margin-left: 10px;
   }
   .friend{
    display: flex;
    flex-direction: column;
    font-size: 15px;
    width: 60%;
    margin-left: 30px;
   }
   .profile-deatils{
    margin-left:-5% ;
   }
   .profile-edit p {
       font-size: 15px;
   }
   .profile-edit button {
       height: 35px;
       width: 75px;
       font-size: 11px;
       margin-left: 5px;
   }
   .profile-edit img {
       height: 25px;
       width: 25px;
       margin-left:0px;
   }
   .name{
    font-size: 17px;
}
}
@media screen and (min-width:350px) and (max-width:500px){
    .post-img img{
        height: 80px;
        width: 80px;
    }
    .profile-img img{
    height: 100px;
    width: 100px;
   }
   .friend{
    display: flex;
    justify-content: space-evenly;
    font-size: 15px;
   }
   .profile-deatils{
    margin-left:4% ;
   }
   .profile-edit p {
       font-size: 18px;
   }
   .profile-edit button {
       height: 35px;
       width: 75px;
       font-size: 11px;
       margin-left: 7px;
   }
   .profile-edit img {
       height: 45px;
       width: 65px;
       margin-left: -1px;
   }
   .name{
    font-size: 21px;
    }
}
@media screen and (min-width:500px) and (max-width:850px){
     .post-img img{
        height: 110px;
        width: 110px;
    }
     .profile-img img{
    height: 120px;
    width: 120px;
   }
   .friend{
    display: flex;
    justify-content: space-evenly;
    font-size: 17px;
   }
   .profile-deatils{
    margin-left:4% ;
   }
}
@media screen and (min-width:850px) and (max-width:1050px){
    
}

</style>