<template>
    <div id="Profil">
        <div id="Introduction">
            <p>
                My name is SeongHan Jo.<br/>
                I am doing web development & product design(web/mobile).<br/>
                The long-term goal is to become an IT professional.
            </p>
            <a href="mailto:lolsh0793@naver.com"><i class="fas fa-envelope"></i> lolsh0793@naver.com</a>
            <div class="subject">what can i do</div>
            <div class="skill" v-for="skill, index in skillset">
                {{index}}
                <span class="level">{{skill}}</span>
            </div>
            <div class="subject">what am i doing</div>
        </div>
    </div>
</template>

<script>
export default {
    data(){
        return{
            skillset : []
        }
    },
    created(){
        this.skillset = {
            'HTML':'intermediate',
            'CSS':'pre-intermediate',
            'JavaSCript':'upper-intermediate',
            'Vue.js':'intermediate',
            'PHP':'pre-intermediate',
            'CodeIgniter':'pre-intermediate',
            'MySQL':'beginner'
        }
    }
}
</script>
<style>
    #Profil{
        text-align: center;
        margin-top: 60px;
        padding-top: 20px
    }
    #Introduction{
        max-width: 960px;
        text-align: left;
        margin: auto;
    }
    #Introduction a{
        color: white;
    }
    #Introduction a:hover{
        color: yellow;
    }
    .subject{
        color: yellow;
        margin-top: 20px;
    }
    .skill{
        position: relative;
        padding: 0px 5px;
        margin-right: 3px;
        display: inline-block;
        background-color: rgba(0, 0, 0, 0.335);
        border-radius: 5px;
    }
    .skill .level{
        position: absolute;
        visibility: hidden;
        bottom:110%;
        left:0;
        z-index: 1;
        white-space:pre;
        color: rgb(48, 48, 48);
        background-color: white;
        padding: 2px 5px;
        border-radius: 5px;
    }
    .skill:hover{
        background-color: rgb(0, 0, 0);
        color:yellow;
    }
    .skill:hover .level{
        visibility: visible;
    }
</style>