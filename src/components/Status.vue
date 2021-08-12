<template>
    <div>
        <div class="status">
                <img :src="newData.image" alt="image"/>
                <h5>{{newData.name}}</h5>
            </div>
            <div>
            </div>
        </div>
</template>
<script>
export default{
    name:'Status',
     props:['newData'],
    data(){
        return{
        }
    }
}
</script>
<style scoped>
.status img{
    height: 110px;
    width: 110px;
    border-radius: 50%;
    border: 3px solid brown;
    margin: 5px;
    margin-bottom:-20px ;
}
.status h5{
    margin-left: 15px;
}
@media screen and (max-width:450px){
    .status img{
        height: 40px;
        width: 40px;
        margin: 5px;
        border: 2px solid brown;
        margin-bottom:-10px ;
    }
    .status h5{
        font-size: 10px;
        padding-left: 5px;
        margin-left:5px ;
    }
}
@media screen and (min-width:450px) and (max-width:700px){
    .status img{
        height:70px;
        width: 70px;
        margin: 10px;
        margin-bottom: -15px;
    }
    .status h5{
        font-size: 13px;
        padding-left:15px ;
    }
}    
</style>