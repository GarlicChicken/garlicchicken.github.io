<template>
    <div id="Portfolio">
        <figure v-for="portfolio, index in shPortfolio">
            <h3>{{index}}</h3>
            <img :src="require('../assets/'+index+'.png')">
            <figcaption>
                <div class="btnGroup">
                    <a class="btn" id="btnApp" :href="'https://garlicchicken.github.io/'+index" target="_blank">APP</a>
                    <a class="btn" id="btnCode" :href="'https://github.com/garlicchicken/'+index" target="_blank"><i class="fas fa-code"></i></a>
                </div>
            </figcaption>
        </figure>
    </div>
</template>

<script>
export default {
    data(){
        return{
            shPortfolio : []
        }
    },
    created(){
        this.shPortfolio = {
          //포트폴리오 추가 -> 아래 객체에 프로퍼티 추가 '리포지터리명(프로젝트명)' : '설명'
          'SNSLoginChat': 'SNS API를 가져와 로그인을 구현했고, Firebase를 저장소로 하는 채팅 앱',
          'ToDoManagement': 'Local Storage를 저장소로 사용해 텍스트의 입력, 출력, 삭제가 가능한 할 일 관리 앱',
          'KakaoFriends':'kakao ix 공채 과제 전형으로 만든 KakaoFriends 개선안, 장바구니(Mylist) 기능을 개선하여 Main(index)페이지에서 Mylist 버튼을 눌렀을 때 사용자가 Mylist에 담은 품목을 확인할 수 있게 하였음.',
          'Weather':'Resource로 외부에서 데이터를 가져와 현재 위치의 날씨를 출력하는 앱',
          'shEditor':'실용성을 강조한 HTML Web Editor'
        };
    }
}
</script>
<style>
    h3{
        color: rgb(78, 78, 78);
        text-align: center;
        margin: 5px 0px 15px 0px;
    }
    /* Portfolio CSS */
    #Portfolio{
        position: relative;
        max-width: 960px;
        column-width: 300px;
        column-gap: 20px;
        margin: auto;
    }
    #Portfolio figure{
        background-color: rgb(255, 255, 255);
        display: inline-block;
        margin: 10px 0px 10px 0px;
        padding: 10px 20px 10px 20px;
        opacity: 0.5;
    }
    #Portfolio figure:hover{
        opacity: 1;
    }
    #Portfolio figure img{
        display: inline-block;
        vertical-align: bottom;
        border-radius: 5px;
        padding-bottom: 0px;
        margin-bottom: 0px;
        width: 100%;
    }
    #Portfolio figure figcaption{
        font-family: 'Nanum Gothic', sans-serif;
        font-size: 0.9rem;
        color: #2b2b2b;
        text-align:justify;
        word-break:break-all;
        line-height: 1.4;
    }
    /* link(button) CSS */
    .btnGroup{
        border: #a0a0a0 1px;
        border-top-style: solid;
        margin: 12px 0px 8px 0px;
        padding: 0;
    }
    .btn{
        width:49%;
        text-decoration: none;
        text-align: center;
        padding:4px 0px 4px 0px;
        margin: 0;
        font-weight: bold;
        display:inline-block;
        transition:all 0.1s;
        background-color: #ffffff;
        color: #616161;
    }
    .btn:active{
        background-color: #616161;
        color: #ffffff;
    }
    .btn:hover{
        background-color: #616161;
        color: #ffffff;
    }
</style>