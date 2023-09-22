<script setup>
    const props = defineProps({
        msg: String,
        
    })

    const emit = defineEmits(['change'])

</script>

<template>
    <div class="bg">
        

        <div class="show-radius">
        <div class="show">
            <div class="show-bg"></div>
            <div class="show-text">
                <div>
                    <h1>Qiu Lan</h1>
                    <p>Founder & CEO</p>
                </div>

                <div>
                    <h1>Andy Zhang</h1>
                    <p>Marketing & Partnerships</p>
                </div>

                <div>
                    <h1>Sherry Liu</h1>
                    <p>Finance & Legal</p>
                </div>

                <div>
                    <h1>John Tang</h1>
                    <p>Support & Care</p>
                </div>

            </div>
        </div>
        </div>

        <div class="title">
            <p>About Us</p>
        </div>

        <div class="text">
            <div>
                <h1>Integrity Innovation Commitment</h1>
                <p>Power Craft 创立于 2019 年，我们是一家以先进动力系统为核心的科技产品公司。公司团队拥有一流的专业素质和研发能力。电机、电池、电控的研发设计，是公司的专业强项。</p>
            </div>
        </div>

        <div class="pic"></div>
        <div class="logo">
           <div> <img src="/xiaomi.png" alt=""></div>
           <div> <img src="/catl.png" alt=""></div>
           <div> <img src="/huawei.png" alt=""></div>
           <div> <img src="/dji.png" alt=""></div>
           <div> <img src="/texas.png" alt=""></div>
           <div> <img src="/tplink.png" alt=""></div>
        </div>
    </div>

    <div class="contact-bg">
        <div class="contact-text">
            <div>
                
                <div>
                    <h1>公司地址</h1>
                    <p>深圳市龙岗区坂田街道五和大道万科星火Online 6 栋 105 室</p>
                </div>
            </div>

            <div>
                
                <div>
                    <h1>联系电话</h1>
                    <p>86-153-5568-6666</p>
                </div>
            </div>

            <div>
                
                <div>
                    <h1>电子邮箱</h1>
                    <p>info@pwr-craft.com</p>
                </div>
            </div>

        </div>
    </div>
</template>

<style scoped>
    .bg{
        position: relative;
        background-color: rgb(44,62,80);
    }



    

    .show-radius{
        position: absolute;
        left: 7.5%;
        top: 350px;
        width: 85%;
        border-radius: 15px;
        overflow: hidden;
    }


    .show-bg{
        background-image: url(/about_show.jpg);
        height: 40vw;
        background-position: center;
        
        background-size: cover;
    }


    @media screen and (min-width: 801px) {
        .show-text{
            display: flex;
            height: 12vw;
        }
    }


    .show-text{ 
        width: 100%;
        background-color: aquamarine;
    }

    .show-text > div{
        padding: 3.2vw 2.8vw;
        flex: 1;
    }


    @media screen and (min-width: 801px) {
        .show-text > div > h1{
            font-size: 1.4vw;
            margin-bottom: 1.4vw;
        }

        .show-text > div > p{
            font-size: 1.1vw;
        }
    }


    @media screen and (max-width: 801px) {
        .show-text > div > h1{
            font-size: 1rem;
            text-align: center;
            margin-bottom: 20px;
        }

        .show-text > div > p{
            font-size: 0.8rem;
            text-align: center;
        }
    }

    .show-text > div > h1{
        
        font-weight:700;
        font-family: var(--font-family);
        
    }

    

    .show-text > div:nth-of-type(1){
        
        background-color: rgb(243,245,247);
    }

    .show-text > div:nth-of-type(2){
        
        background-color: rgb(236, 238, 240);
    }

    .show-text > div:nth-of-type(3){
        
        background-color: rgb(226, 230, 234);
    }

    .show-text > div:nth-of-type(4){
        
        background-color: rgb(218, 222, 227);
    }

    .title{
        height: 500px;
        padding-top: 220px;
    }

    .title > p{
        text-align: center;
        font-size: 3.5rem;
        color: rgb(255,255,255);
        font-weight:750;
    }


    @media screen and (min-width: 801px){
        .text{
            padding: 46vw 0px 100px;
        }

        .text > div{
        width: 58%;
        margin: 0 auto;
    }
    }

    @media screen and (max-width: 801px){
        .text{
            padding: 86vw 0px 100px;
        }

        .text > div{
             width: 85%;
             margin: 0 auto;
    }
    }

    .text{
        
        
        background-color: rgb(255,255,255);
        text-align: center;
    }

    

    .text > div > h1{
        color: var(--hover-color-green);
        font-size: 3rem;
        margin-bottom: 100px;
        font-family: var(--font-family);
        font-style: italic;
        
    }

    .text > div > p{
        font-size: 1.5rem;
        font-weight: bolder;
        text-indent: 1rem;
    }

    .pic{
        height: 600px;
        background-image: url(/about_pic.jpeg);
        background-size: cover;
        background-position: center;
    }

    .logo{
        height: 300px;
        display: flex;
        justify-content:space-between;
        align-items: center;
        padding: 0px 10%;
    }

    

    .logo > div > img{
        display: block;
        margin: 0 auto;
        width: 80%;
        
    }



    .contact-bg{
        height: 300px;
        background-color:rgb(254,254,254);
    }


    @media screen and (min-width: 1101px) {
        .contact-text{
            display: flex;
        }

        .contact-text > div{
            width: 33%;
            background-size: 6%;
        }

        
        
    }


    @media screen and (max-width: 1101px){
        .contact-text > div{
            
            background-size: 20px;
        }

    }

    .contact-text{
        width: 80%;
        margin: 20px auto 20px;
        background-color: rgb(255,255,255);
        padding: 40px 30px;
        
        justify-content: space-between;
        border-radius: 15px;
        box-shadow: var(--box-shadow);
    }

    .contact-text > div{
        
        padding: 30px 60px;

    }

    .contact-text > div > div > h1{
        font-size: 1.2rem;
        margin-bottom: 30px;
        text-align: center;
    }

    .contact-text > div > div > p{
        font-size: 0.95rem;
        line-height: 1.5rem;
        text-align: center;
    }

    .contact-text > div{
        background-position: 22% 18% ;
        background-repeat: no-repeat;
    }

    .contact-text > div:nth-of-type(1){
        background-image:   url(/position.png) ;
        
    }

    .contact-text > div:nth-of-type(2){
        background-image:   url(/phone.png) ;
        
    }

    .contact-text > div:nth-of-type(3){
        background-image:   url(/email.png) ;
        
    }

    

    

    
    
</style>