<script setup>
    import {ref} from 'vue';
    import { onMounted } from 'vue';

    const props = defineProps({
        msg: String,
        
    })

    const emit = defineEmits(['change'])

    function clickWind() {
        emit('change','wind')
    }

    function clickRobot() {
        emit('change','robot')
    }

    function clickShip() {
        emit('change','ship')
    }

    function clickX() {
        emit('change','x')
    }

    function clickOne() {
        emit('change','one')
    }

    function clickTwo() {
        emit('change','two')
    }


</script>

<template>
    
        <div id="one" class="index-bg">
            <div class="index-bg-color">
                <div class="index-bg-Text">
        
        <h1>TOGETHER WITH POWER CRAFT</h1>
        <h1>SHIFT TO A SUSTAINABLE WORLD</h1>

            </div>
            </div>
        </div>
        
        
    
    
    <div class="index-content-bg">
    <div class="index-content">
        <div class="dire-pic">
            <div><div class="title-lv2">工业机器人</div></div>
            <div><div class="title-lv2">电动船舶</div></div>
            <div><div class="title-lv2">便携冰箱</div></div>
            <div><div class="title-lv2">新能源</div></div>
        </div>

        <div class="dire-text">
            
                <div>
                    <div><span>#1</span><span>工业机器人</span></div>
                    <div>
                        <p>我们致力于为企业生产安全、灵活和易于使用的多轴工业机械臂的电控方案。我们开发的协作式机器人，帮助用户实现自动化，简化重复性工业。为企业的员工赋能，将他们从低附加值劳动中解放出来，从而为公司创造更多价值。</p>
                    </div>
                </div>
                <div>
                    <div><span>#2</span><span>电动船舶</span></div>
                    <div>
                        <p>船舶电动化是当前的行业趋势。装载我们的电控方案的电动船舶，不仅减少了汽油/柴油对于水体的污染，还具备无噪音、无异味、无油污、驾驶容易、保养简单等优势，能够给用户带来更好的体验</p>
                    </div>
                </div>
            
            
                <div>
                    <div><span>#3</span><span>便携冰箱</span></div>
                    <div>
                        <p>我们全新设计的便携制冷产品系列，利用最新的节能技术，打造一流的制冷体验。</p>
                    </div>
                </div>
                <div>
                    <div><span>#4</span><span>新能源</span></div>
                    <div>
                        <p>我们为新能源产业客户提供专业的工业电控解决方案，助力世界向可持续能源发展。</p>
                    </div>
                </div>
            
        </div>

        <div class="recom-products">
            <div>
                <div class="recom-products-title">Power Fridge X</div>
                <div class="recom-products-text">强力便携冰箱.</div>
                <div class="recom-products-a"><a href="#/Chanpin" @click="clickX">了解更多</a></div>
            </div>
            <div class="recom-products-tu"><img src="/recom_1.png" alt=""></div>
        </div>

        <div class="main-products">
            <div class="main-products-title title-margin">
                <div class="title-lv1">主打产品</div>
                <a href="#/Chanpin" >查看更多</a>
            </div>

            <div class="main-products-content">
                <div>
                    <div class="tu-wen">
                        <div class="main-products-content-tu"><img src="/one.png" alt="图片无法显示噢"></div>
                        <div class="main-products-content-title">Power Fridge One</div>
                        <div class="title-mini">便携冰箱</div>
                    </div>
                    <a href="#/Chanpin" @click="clickOne">阅读更多</a>
                </div>

                <div>
                    <div class="tu-wen">
                        <div class="main-products-content-tu"><img src="/two.png" alt="图片无法显示噢"></div>
                        <div class="main-products-content-title">Power Fridge Two</div>
                        <div class="title-mini">便携冰箱</div>
                    </div>
                    <a href="#/Chanpin" @click="clickTwo">阅读更多</a>
                </div>

                <div>
                    <div class="tu-wen">
                        <div class="main-products-content-tu"><img src="/x.png" alt="图片无法显示噢"></div>
                        <div class="main-products-content-title">Power Fridge X</div>
                        <div class="title-mini">便携冰箱</div>
                    </div>
                    <a href="#/Chanpin" @click="clickX">阅读更多</a>
                </div>
                
            </div>

        </div>

        <div class="industry">
            <div class=" title-lv1 title-margin">业界动态</div>

            <div class="industry-content">


                <div >
                    <div class="industry-content-tu">
                        <img src="/big_wind.png" alt="无图片">
                    </div>

                    <div class="industry-content-text">
                        <div class="industry-content-text-1">
                            <div class="text-mini">新能源</div>
                            <div class="title-lv2">国家能源局：风光大基地应开尽开、能开尽开 </div>
                            <div>近日，国...</div>
                        </div>
                        <a href="#/Zixun" @click="clickWind">继续阅读</a>
                    </div>
                </div>



                <div >
                    <div class="industry-content-tu">
                        <img src="/robot.png" alt="无图片">
                    </div>
                    
                    <div class="industry-content-text">
                        <div class="industry-content-text-1">
                            <div class="text-mini">工业机器人</div>
                            <div class="title-lv2">中国工业机器人产业：拥抱发展新机遇  </div>
                            <div>在2021年…</div>
                        </div>
                        <a href="#/Zixun" @click="clickRobot" >继续阅读</a>
                    </div>
                </div>



                <div >
                    <div class="industry-content-tu">
                        <img src="/shipping.png" alt="无图片">
                    </div>
                    
                    <div class="industry-content-text">
                        <div class="industry-content-text-1">
                            <div class="text-mini">电动船舶</div>
                            <div class="title-lv2">船舶电动化“风起云涌”  </div>
                            <div>浩浩荡荡…</div>
                        </div>
                        <a href="#/Zixun" @click="clickShip" >继续阅读</a>
                    </div>
                </div>

                
                

            </div>
        </div>
    </div>
    </div>

    <div class="subscribe">
        <div class="subscribe-title ">订阅新闻</div>
        <form class="subscribe-form" action="" method="post">
            <label for="mail">电子邮箱</label>
            <input type="email" id="mail" name="usereamil" placeholder="请输入您的电子邮箱*">
            <button type="submit">订阅</button>
        </form>
    </div>
    

</template>

<style scoped>



[class='index-content'] > div > div{
    border-radius: var(--box-radius);
}



/* main hover */

.main-products-content-tu,.industry-content > div{
    border-radius: var(--box-radius);
}

.main-products-content [class*='title']{
    transition:var(--transition-sd-02);
    
}

.main-products-content [class*='title']:hover{
    color: var(--hover-color-green);
    cursor: pointer;
}

.main-products-content-tu > img{
    transition: var(--transition-sd-03); 
}

.main-products-content-tu:hover > img{
    transform: scale(1.1);
}

/* industry hover */

.industry-content [class*='title']{
    transition: var(--transition-sd-02);
    
}

.industry-content [class*='title']:hover{
    color: var(--hover-color-green);
    cursor: pointer;
}

.industry-content-tu > img{
    transition: var(--transition-sd-03);
}

.industry-content > div:hover .industry-content-tu > img{
    transform: scale(1.1);
}

/* recom hover */

.recom-products-a > a:hover{
    background-color: var(--font-body-color);
}

/* diertext hover */

.dire-text div,.dire-text p{
    transition: var(--transition-sd-02);
}

.dire-text > div:hover {
    background-color: var(--hover-color-green);
    
}

.dire-text > div:hover > div{
    color: var(--font-whilt);
}

.dire-text > div:hover > div > p{
    color: var(--box-grey);
}

/* direpic hover  */

.dire-pic div{
    transition: var(--transition-sd-02);
}

.dire-pic > div:hover > div{
    color: var(--font-whilt);
}

.dire-pic > div:hover:nth-of-type(1){
    background-color: rgb(255,199,80);
}

.dire-pic > div:hover:nth-of-type(2){
    background-color: rgb(62,175,124);
}

.dire-pic > div:hover:nth-of-type(3){
    background-color: rgb(9,145,127);
}

.dire-pic > div:hover:nth-of-type(4){
    background-color: rgb(0, 0, 0);
}

/* hover end */

a{  
    transition:var(--transition-sd-02);
    display:inline-block;
    padding: 15px 20px;
    background-color: var(--box-grey);
    text-decoration: none;
    color: rgb(44,62,80);
    border-radius:5px;
    font-weight: var(--font-weight);
    
}

a:hover{
    background-color: var(--hover-color-green);
    color: var(--font-whilt);
}



.title-lv1{
    font-size: var(--font-size-title-lv1);
    font-weight: var(--font-weight);
}

.title-lv2{
    font-size: var(--font-size-title-lv2);
    font-weight: bolder;
    
}

.text-mini{
    font-size: var(--font-size-text-mini);
    font-weight: bold;
    color: rgb(44,62,80);
}


.tu-wen > div{
    margin-bottom: 20px;
}

.title-margin{
    margin-bottom: 50px;
}





                                                        /* bg style */

.index-bg{
    width: 100%;
    
    background-attachment: fixed;
    
    background-color: black;
    background-position: center;
    background-position-y: 50%;
    background-size: cover;
    background-image: url(/index_bg.jpg);
}

.index-bg-color{
    background-attachment: fixed;
    
    width: 100%;
    
    background-color:rgba(0, 0, 0,0.4);
    
}

.index-bg-Text{
    width: 85%;
    margin: 0 auto;
    height: 1000px;
    
}

.index-bg-Text h1{
    text-align: center;
    font-weight: var(--font-weight);
    
}

h1:nth-of-type(1){   
    font-size: 3.6rem;    
    color:var(--font-whilt);
    
}

h1:nth-of-type(2){
    position:relative;
    font-size: 2.8rem;
    color:var(--font-green);
}

@media screen and (max-width:501px){
    .index-bg-Text{
        padding-top: 200px;
        overflow-wrap: break-word;
    }

    h1:nth-of-type(2){
        top: 10vh;
    }
}

@media screen and (min-width: 501px) {
    .index-bg-Text{
        padding-top: 380px;
    }

    h1:nth-of-type(2){ 
        top: 4.5vw;
    }
}





                                            /* main content style  start */

.index-content-bg{
    width: 100%;
}

.index-content-bg{
    background-color: rgb(255, 255, 255);
    padding-top: 130px;
}

.index-content{
    width: 85%;
    margin: 0 auto;
    max-width: 1900px;
}

.index-content > div{
    margin-bottom: 100px;
}





                                                /* dier-pic style */

@media screen and (max-width:501px) {
    .dire-pic > div{
    height: 85vw;
    margin-bottom:var(--margin-bottom);
    }

    
}


@media screen and (min-width: 501px) {
    .dire-pic{
    display: grid;
    grid-template-columns: 2fr 1fr 1fr;
    gap: 2vw;
    grid-auto-rows: 17vw;
    }

    
}


.dire-pic > div{
    box-shadow: var(--box-shadow);
    background-color: var(--box-whilt);
}

.dire-pic div:nth-of-type(1){
    
    grid-column: 1/2;
    grid-row: 1/3;
}

.dire-pic div:nth-of-type(2){
    
    grid-column: 2/4;
    grid-row: 1;
}

.dire-pic div:nth-of-type(3){
    
    grid-column: 2;
    grid-row: 2;
}

.dire-pic div:nth-of-type(4){
    
    grid-column: 3;
    grid-row: 2;
}

.dire-pic > div > div{
    width: 100%;
    height: 100%;
    background: no-repeat;
    padding: 3.5vw;
    
    
}

@media screen and (min-width:501px) {
    .dire-pic > div > div{
        font-size: 1.3vw;
    }
}

.dire-pic div:nth-of-type(1) > div{
    background-size: contain;
    background-position: center;
    background-image: url(/pic_1.png);
}

.dire-pic div:nth-of-type(2) > div{
    background-image: url(/pic_2.png);
    background-position-x: 100%;
    
    
}

@media screen and (min-width:501px){
    .dire-pic div:nth-of-type(2) > div{
        background-position-y: 180%;
        background-size: 35%;
    }
   
}

@media screen and (max-width:501px){
    .dire-pic div:nth-of-type(2) > div{
        background-position-y:100%;
        background-size: 70%;
    }
    
}

.dire-pic div:nth-of-type(3) > div{
    background-image: url(/pbx_3.png);
    
    background-position-y:100%;
    background-size: 100%;
}



.dire-pic div:nth-of-type(4) > div{
    background-size: contain;
    background-position: center;
    background-image: url(/pic_4.png);
}






                                                /* dire-text style */


@media screen and (min-width: 1051px) {
    .dire-text{
    display: flex;
    
    justify-content:space-between;
}

    .dire-text > div{
    
    width: 23%;
    
}

}

@media screen and (min-width:501px) and (max-width:1051px) {
    .dire-text{
        display: grid;
        grid-template-columns: 1fr 1fr;
        gap: 40px;
    }

    .dire-text > div:nth-of-type(1){
        grid-column: 1;
    }

    .dire-text > div:nth-of-type(2){
        grid-column: 2;
    }

    .dire-text > div:nth-of-type(3){
        grid-column: 1;
        grid-row: 2;
    }

    .dire-text > div:nth-of-type(4){
        grid-column: 2;
        grid-row: 2;
    }
}

@media screen and (max-width: 501px) {
    .dire-text > div{
    
    margin-bottom:var(--margin-bottom);
    
}
}


.dire-text > div{
    background-color: var(--box-grey);
    padding: 24px;
    min-height: 300px;
}
.dire-text > div > div > span{
    
    font-weight: var(--font-weight);
    display: inline-block;
    height: 50px;
}

.dire-text > div > div > span:nth-of-type(1){
    width: 1.5rem;
    border-bottom: 2px solid rgb(213, 211, 211);
}

.dire-text > div > div:nth-of-type(2){
    color: var(--font-grey);
    margin-top: 20px;
}




                                                        /* recom-products style */

@media screen and (min-width: 1051px) {
    .recom-products{
        display: flex;
        justify-content: space-between;
    }

    .recom-products-tu{
        width: 250px;
        margin-right: 110px;
        margin-top: 20px;
    }

    .recom-products-title{
        font-size: var(--font-size-super);
        font-weight:bolder;
    }   

    .recom-products-a > a{
        padding: 18px 32px;
        font-weight: bolder;
    
    }
}

@media screen and (max-width: 1051px) {

    .recom-products-tu{
        max-width: 250px;
        margin:  20px auto 0px;
    }

    

    .recom-products-a{
        width: 104px;
        margin: 0 auto;
    }

    .recom-products-text,.recom-products-title{
        text-align: center;
    }

    .recom-products-title{
        font-size:7vw;
        font-weight:bolder;
    }  
}
.recom-products{
    
    border-radius: var(--box-radius);
    min-height: 420px;
    background-image: url(/recom_bg.png);
    background-position: center;
    background-size: cover;
    padding: 75px;
}

.recom-products img{    
    max-width:100%;  
    }

.recom-products > div > div{
    margin-top: 30px;
    color: rgb(255, 255, 255);
}





.recom-products-text{
    font-size: 1.2rem;
}




                                                /* main-products style */

.main-products-title{
    display: flex;
    justify-content: space-between;
    
}




@media screen and (min-width:501px) {
    .main-products-content{
        display: grid;
        grid-template-columns: 1fr 1fr 1fr;
        gap: 2vw;
    }  
}

@media screen and (max-width: 501px) {
    .main-products-content > div{
        margin-bottom:var(--margin-bottom);
    }
}

.main-products-content-tu{
    overflow: hidden;
}

.main-products-content img{
    width: 100%;
    height: 100%;
    display: block;
}

.main-products-content-title{
    font-weight: bolder;
}



                                                    /* industry-content style */

@media screen and (min-width: 1051px) {
    .industry-content{
        display: grid;
        grid-template-columns: 1fr 1fr 1fr;
        gap: 40px;
    } 

    .industry-content-tu{
        height: 20vw;
        
        
    }
}

@media screen and (max-width: 1051px) and (min-width: 501px){
    .industry-content{
        display:grid;
        grid-template-columns: 1fr 1fr 1fr 1fr;
        
        gap: 40px;
    }

    .industry-content > div:nth-of-type(1){
        grid-column: 1/3;
    }

    .industry-content > div:nth-of-type(2){
        grid-column: 3/5;
    }

    .industry-content > div:nth-of-type(3){
        grid-column: 2/4;
        grid-row: 2;
    }

    .industry-content-tu{
        height: 30vw;
    }
}

@media screen and (max-width: 501px) {
    .industry-content > div{
        margin-bottom: var(--margin-bottom);
    }

    .industry-content-tu{
        height: 70vw;
    }
}



.industry-content > div{
    box-shadow: var(--box-shadow);
    overflow: hidden;
    
}

.industry-content-tu{
    overflow: hidden;
}

.industry-content img{
    width: 100%;
    height: 100%;
    margin-bottom: 20px;
}

.industry-content-text{
    padding: 40px;
    position: relative;
}

.industry-content-text-1 > div{
    margin-bottom: 20px;
}

.industry-content-text-1 > div:nth-of-type(3){
    font-weight: lighter;
}

.industry-content-text-1{
    min-height: 160px;
}




                                            /* subscribe style */

.subscribe{
    width: 100%;
    height: 450px;
    background-color: rgb(24,28,31);
}

.subscribe-title{
    padding-top: 120px;
    color: rgb(255, 255, 255);
    text-align: center;
    font-size: 2.2rem;
    font-weight: bolder;
}

.subscribe-form{
    display: flex;
    justify-content: center;
    position: relative;
    margin-top: 35px;
    align-items: center;
    font-family: inherit;
    font-size: 100%;
}

.subscribe-form > label{
    position: absolute;
    left: -100px;
}

.subscribe-form > input{
    color: rgb(246, 242, 242);
    background-color: rgb(0,0,0);
    border: 0;
    
    height: 60px;
    border-radius: 8px;
    font-size: 1rem;
    padding-left: 15px;
}

@media screen and (min-width: 1051px) {
    .subscribe-form > input{
        width: 500px;
    }

    .subscribe-form{
        flex-direction: row;
    }

    .subscribe-form > button{
        margin-top: 0px;
        margin-left:18px;
    }
}

@media screen and (max-width:1051px) {
    .subscribe-form > input{
        width: 50%;
    }

    .subscribe-form{
        flex-direction: column;
    }

    .subscribe-form > button{
        margin-left: 0;
        margin-top: 15px;
    }
}

input:focus{
    background-color: rgb(14, 13, 13);
}

.subscribe-form > button{
    border: 0;
    background-color:rgb(62,175,124);
    padding: 20px 36px;
    
    border-radius: 8px;
    font-size: 1rem;
    color: rgb(255, 255, 255);
}
</style>