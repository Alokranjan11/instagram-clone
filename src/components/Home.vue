<template>
    <div class="home">
        <div>
           <Header></Header>
        </div>
        <div class="home-status">
             <div v-for="data in post" :key="data.id">
                <Status :newData="data"/>
            </div>
        </div>
        <!-- <div class="post-view"> -->
            <div class="post">
            <div v-for="data in post" :key="data.id">
                <Post :newData="data"/>
            </div>
        </div>
        <!-- </div> -->
    </div>
</template>
<script>
import Header from './Header.vue'
import Status from './Status'
import Post from './Post.vue'
export default{
    name:'Home',
    components:{
        Header,
        Post,
        Status,
    },
    data(){
        return{
            post:[
                {id:1,image:"/img/alok.jpg",name:"raj.alok07",title:"test title",likeImage:"/img/like.jpg",like:10,comment:[
                    {id:1,comment:"Awesome"}
                ]},
                 {id:2,image:"/img/car.jpg",name:"Mercedes",title:"test title",likeImage:"/img/like.jpg",like:17,comment:[
                    {id:2,comment:"nice car"}
                ]},
                 {id:3,image:"/img/virat.jpeg",name:"virat.kohli",title:"test title",likeImage:"/img/like.jpg",like:15,comment:[
                    {id:3,comment:"well played"}
                ]},
                 {id:4,image:"/img/jeep.jpg",name:"Jeeep",title:"test title",likeImage:"/img/like.jpg",like:12,comment:[
                    {id:4,comment:"This is also nice car"}
                ]},
            ]

        }

    }
}
</script>
<style scoped>
/* .post-view{
    
} */
.home{
    display: flex;
    flex-direction: column;
}
.post{
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    /* border: 2px solid red; */
}
/* .post-view{
    width:100%;
    margin-bottom: 5px;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    border:2px solid red;
} */
.home-status{
    display: flex;
    margin-top: 10px;
    border-top: 2px solid rgb(209, 202, 202);
    border-bottom: 2px solid rgb(209, 202, 202);
    border-left: 2px solid rgb(209, 202, 202);
}
@media screen and (max-width:450px) {
    .home-status{
        width: 100%;
    }
}
@media screen and (min-width:450px) and(max-width:700px){
    .home-status{
        width: 100%;
    }
}
</style>