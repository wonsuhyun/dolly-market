<template>
    <div class="header-wrap">
        <span class="title">
            <nuxt-link to="/" >
            {{ headerTitle }}
            </nuxt-link>
        </span>
        <div class="search">
            <input type="text" id="searchArea" class="search-area" @keyup="enterKey"/><button type="button" id="serchBtn" @click="btnClickEvent">Search</button>
        </div>
        <div>te</div>
    </div>
</template>
<script>
export default {
    data(){
        return {
            headerTitle:"Dolly Market"
        }
    },
    methods:{
        enterKey:function(e){
            if(e.keyCode==13){
                console.log("keyup")
                $("#serchBtn").trigger("click")
            }
        },
        btnClickEvent:function(e){
            console.log("triggered")
        }
    }
}
</script>
<style>

.header-wrap {
    width:1000px;
    margin:0 auto;
    padding:30px 0;
    overflow:hidden;
}
.header-wrap > span{
    float:left
}
.header-wrap > .search{
    float:right
}
.header-wrap > .search input, .header-wrap > .search button{
    height:40px;
    padding: 0 20px
}
.header-wrap > .search button{
    border:none;
    background:#5e5e5e;
    color:#fff;
}
.header-wrap > .search input{
    width:300px;
    border:1px solid #d2d2d2
}
.header-wrap span.title{
    font-weight:700;
    font-size:20px;
    font-family:'Roboto';
}
</style>