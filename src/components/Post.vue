<template>
    <div class="post-main">
        <div class="profile">
            <img :src="newData.image" alt="image"/>
            <h5>{{newData.name}}</h5>
        </div>
        <div class="post-img">
            <img :src="newData.image" alt="image"/>
        </div>
        <div class="like-comment">
            <div class="like">
             <img @click="like(newData)" :src="newData.likeImage" alt="like"/>   
            <h4>{{newData.like}}like</h4>
        </div>
        <div>
            <p>{{newData.comment.length}}comments</p>
        </div>
        <div v-for="data in newData.comment" :key="data.id">
            <p>{{data.comment}}</p>
        </div>
        <div class="comment">
            <img src="img/emoji.jpg" alt="image"/>
            <input v-model="enter" type="text" placeholder="Add comment"/>
            <button @click="commentPush(newData)">Post</button>
        </div>
        </div>
        
    </div>
</template>
<script>
export default{
    name:'Post',
    props:['newData'],
    data(){
        return{
            enter:"",
        }
    },
    methods:{
        like(data){
            data.like++
            console.table(data)
        },
        commentPush(data){
            data.comment.push({id:4,comment:this.enter})
            this.enter=""
            console.table(data)
        }
    }
}
</script>
<style scoped>
.post-main{
    border: 1px solid rgb(209, 202, 202);
     /* width:100%; */
    display: flex;
    flex-direction: column;
    margin: 24px;
}
.like-comment{
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    padding:10px;
}
.post-img img{
    height:500px;
    width: 500px;
}
.profile{
    display: flex;
}
.profile img{
    height: 50px;
    width: 50px;
    border-radius: 50%;
    margin: 10px;
    border: 3px solid brown
}
.like{
    display: flex;
    align-items: center;
}
.like img{
    height: 25px;
    width: 30px;
    margin: 5px;
    cursor: pointer;

}
.comment{
    display: flex;
    justify-content: space-around;
}
.comment img{
    height: 50px;
    width: 150px;
}
.comment button{
    height: 50px;
    width: 40%;
    border: none;
    background-color: #fefefe;
    color: rgb(145, 145, 231);
    font-size: 19px;
    cursor: pointer;
}
.comment input{
    border: none;
    outline: none;
    width: 30%;
    margin-left:-7px ;
}
@media screen and  (max-width:510px){
    .profile img{
       height: 30px;
       width: 30px;
       border: 1px solid brown
    }
    .post-main{
        width: 85%;
    }
    .post-img img{
    height:250px;
    width: 250px;
}
    .profile h5{
        font-size: 8px;
    }
    .like img{
    height: 20px;
    width: 20px;
    }
    .comment img{
        height: 45px;
        width: 70px;
    }
    .comment button{
        width: 50%;
        height: 25px;
    }
    .comment input{
        width:100%;
        height:15px;
    } 
}

@media screen and (min-width:510px) and (max-width:850px){
    
    .profile img{
       height: 40px;
       width: 40px;
       border: 2px solid brown
    }
      .comment button{
        width: 35%;
    } 

}
</style>