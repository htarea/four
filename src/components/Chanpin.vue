<script setup>
    const props = defineProps({
        msg: String,
        
    })

    const emit = defineEmits(['change'])
</script>

<template>
    <div class="nav">
        <div class="nav-title">
            <p><span>便携冰箱</span></p>
        </div>
        <div class="nav-content">
            <div>               
                    <div class="nav-content-one">
                        <a  @click="msg = 'one'"><img src="/one.png" alt="图片无法显示噢"></a>
                        <div class="nav-content-one-title">Power Fridge One</div>
                    </div>               
            </div>

            <div>               
                    <div class="nav-content-two">
                        <a  @click="msg = 'two'"><img src="/two.png" alt="图片无法显示噢"></a>
                        <div class="nav-content-two-title">Power Fridge Two</div>
                    </div>               
            </div>

            <div>               
                    <div class="nav-content-x">
                        <a  @click="msg = 'x'"><img src="/x.png" alt="图片无法显示噢"></a>
                        <div class="nav-content-x-title">Power Fridge X</div>
                    </div>               
            </div>
            <div></div>
            <div></div>
            <div></div>
            <div></div>
            
        </div>
    </div>

    <div class="main">

        <div class="title">
            <p v-if="msg === 'x'"><a @click="msg = 'one'">便携冰箱</a><span> / </span>POWER FRIDGE X</p>
            <p v-else-if="msg === 'one'"><a @click="msg = 'one'">便携冰箱</a><span> / </span>POWER FRIDGE ONE</p>
            <p v-else-if="msg === 'two'"><a @click="msg = 'one'">便携冰箱</a><span> / </span>POWER FRIDGE TWO</p>
        </div>

        <div class="content">
            <div v-if="msg ==='x'" class="content-tu-x"></div>
            <div v-else-if="msg ==='one'" class="content-tu-one"></div>
            <div v-else-if="msg ==='two'" class="content-tu-two"></div>
            
            <div class="content-text">
                <div v-if="msg === 'x'">
                    <h1>Power Fridge X</h1>
                    <p>Whether you're college-bound or simply want a little extra refrigerator space in your home, the Power Fridge X. ft. Mini Refrigerator has the storage options you're looking for. The sleek appearance is matched by its well-designed interior, which includes a can dispenser to conveniently keep soda in the door, while additional door shelves provide space for other frequently used items. Its two glass shelves are easy to clean, and the qualified design helps save on energy costs without sacrificing performance.</p>                    
                    <p><span>分类：</span><a @click="msg = 'one'">便携冰箱</a></p>
                </div>

                <div v-else-if="msg === 'one'">
                    <h1>Power Fridge One</h1>
                    <p>Power Fridge One Mini Refrigerator is perfect for personal space, travel, office, dorm, road trip, boating, camping, tailgating, commuting, and more; Small size and stylish design for easy commuting; Use this mini-fridge to store your snacks, beverages, sodas, baby bottles, skincare products, and even hot soups and meals.</p>
                    <p><span>分类：</span><a @click="msg = 'one'">便携冰箱</a></p>
                </div>

                <div v-else-if="msg === 'two'">
                    <h1>Power Fridge two</h1>
                    <p>

                        The Power Fridge Two Mini Fridge boasts efficiency and durability in one stylish, compact unit that can comfortably store up to 18 twelve-ounce soda cans.

                        Featuring a roomy 15-liter capacity, take The Power Fridge Two anywhere you need drinks and snacks close by: at work or school, or on your next trip or tailgate party.

                        Exclusive Technology features a unique cooling system. The Power Fridge Two is quiet, cost-effective, and goes from cooling to warming with one quick switch.

                        The Power Fridge Two is 100% environmentally friendly—its advanced semiconductor operation uses no refrigerants or Freons.
                    </p>
                    <p><span>分类：</span><a @click="msg = 'one'">便携冰箱</a></p>
                </div>

            </div>
            
        </div>
    </div>
</template>

<style scoped>



.nav-title{
    
    padding: 60px 7.5% 10px;
    border-bottom: 1px solid rgb(237,239,242);
    
}

.nav-title > p > span{
    transition: var(--transition-sd-02);
    
    font-size: 0.9rem;
}

.nav-title > p > span:hover{
    color: var(--hover-color-green);
    cursor: var(--hover-pointer);
}

.nav-content{
    width: 100%;
    overflow-x: auto;
    padding: 20px 7.5% 0px;
    
    display: grid;
    gap: 50px;
    grid-template-columns: repeat(7,1fr);
    grid-auto-rows: 200px;
}

.nav-content > div > div{
    position: relative;
    width: 130px;
    height: 100%;
    
}


.nav-content > div > div > a > img{
    transition: var(--transition-sd-03);
    position: absolute;
    width: 90%;
    border-radius: 8px;
    left: 5%;
    top: 5%;
}

.nav-content > div > div > a > img:hover{
    transform: scale(1.1);
    cursor: var(--hover-pointer);
}

.nav-content > div > div > div{
    transition: var(--transition-sd-02);
    position: absolute;
    bottom: 15%;
    left: 5%;
    font-size: 0.9rem;
}

.nav-content > div > div > div:hover{
    cursor: var(--hover-pointer);
    color: var(--hover-color-green);
}


.main{
    width: 85%;
    height: 1200px;
    margin: 0 auto;
    padding-top: 150px;
    
}
.title > p {
    font-size:0.75rem;
    
    
}

.title > p > a{
    color: var(--hover-color-green);
    font-weight:bold;
    cursor: pointer;
}

.title > p > span{
    padding: 0 4px;
    
    font-size: 0.9rem;
}

@media screen and (min-width: 765px){
    .content{
        display: flex;
        justify-content:space-between;
    }

    .content-tu-x,.content-tu-one,.content-tu-two{
        width: 50%;
        height: 58vw;
    }

    .content-text{
        width: 46%;
    }

}

@media screen and (max-width: 765px){
    .content-tu-x,.content-tu-one,.content-tu-two{
        width: 100%;
        height: 500px;
    }

    .content-text{
        width: 100%;
        margin-top: 60px;
        padding-bottom: 100px;
    }

}
.content{
    
    
    margin-top: 40px;
    
}

.content-tu-x{
    
    background-image: url(/x_big.png);
    background-size: cover;
    background-position: center;
    
}

.content-tu-one{
    
    background-image: url(/one_big.png);
    background-size: cover;
    background-position: center;
    
}

.content-tu-two{
    
    background-image: url(/two_big.png);
    background-size: cover;
    background-position: center;
    
}



.content-text > div > h1{
    font-size:calc(var(--font-size-title-lv1) + 0.2rem );
    margin-bottom: 40px;
}

.content-text > div > p:nth-of-type(1){
    font-size: 1.1rem;
    line-height: 2rem;
    font-family:'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
    padding-bottom: 30px;
    border-bottom: 1px solid rgb(237,239,242);
}

.content-text > div > p:nth-of-type(2){
    font-size: 0.8rem;
    margin-top: 30px;
}

.content-text > div > p:nth-of-type(2) > span{
    font-weight:bold;
}

.content-text > div > p:nth-of-type(2) > a{
    color: var(--font-grey);
}

.content-text > div > p:nth-of-type(2) > a:hover{
    color: var(--hover-color-green);
    cursor: var(--hover-pointer);
}

</style>