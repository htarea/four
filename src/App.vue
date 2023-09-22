<script setup>
  import { ref, computed ,onMounted} from 'vue'
  import main from './components/main.vue'
  import Chanpin from './components/Chanpin.vue'
  import Zixun from './components/Zixun.vue'
  import about from './components/about.vue'

  onMounted(funScroll)
  
  

  function funScroll() {
    let bo ;
    let oldbo = 0;
    let time = 0;
    
    let nav = document.querySelectorAll('.nav')[0];
    let product = document.querySelector('.product');
    let navText = document.querySelectorAll('.nav-text > a');
    let bgBlack = document.querySelector('.bg-black');

    window.addEventListener('scroll',throttle(paScroll,500));
    
    
    product.addEventListener('mouseover',viewProA);
    product.addEventListener('mouseout',viewProB);
    product.addEventListener('touchstart',viewProA);
    navText[1].addEventListener('touchstart',viewProA);
    bgBlack.addEventListener('touchstart',viewProB);

    function viewProA() {
      product.style.opacity = '1';
      product.style.left = '0';
      product.style.width = '100%';
      product.style.height = '400px';
      bgBlack.style.zIndex = '98';
      bgBlack.style.opacity = '1';

    }

    function viewProB() {
      product.style.opacity = '0';
      product.style.left = '46.5%';
      product.style.width = '0';
      product.style.height = '0';
      bgBlack.style.zIndex = '-1';
      bgBlack.style.opacity = '0';
    }

    

    function throttle(func,wait) {
      
      return function() {
        if(!time) {
          time = Date.now();
        }

        if(Date.now() - time > wait) {
          func.apply(this);
          time = Date.now();
          
        }
      }
    }

  

    function paScroll() {
      bo = document.documentElement.scrollTop;
      
      if(oldbo > bo){
        nav.style.top = '0px';
        oldbo = bo;
        
        navText.forEach((x) => {
          x.style.color = 'var(--hover-color-green)';
        })
      }
       else if(oldbo < bo){
        nav.style.top = '-80px';
        oldbo = bo;
        
        navText.forEach((x) => {
          x.style.color = 'rgb(255,255,255)';
        })
      }
    }
    
  }
  
  


  const router = {
    '/Index': main,
    '/Chanpin': Chanpin,
    '/Zixun': Zixun,
    '/about': about
  }

  const currentPath = ref('#/Index')
  
  window.location.hash = currentPath.value

  window.addEventListener('hashchange',function() {
    currentPath.value = this.window.location.hash;
    document.documentElement.scrollTop = 0;
    
  })

  const currentView = computed(() => {
    return router[currentPath.value.slice(1)]
  })


  const msgs = ref(null)
  

</script>

<template>
  <div class="bg-black"></div>
  <header>

    <div class="nav"></div>

    <div class="nav-text">

      <a href="#/Index">首页</a>
      <a >产品</a>
      <a href="#/about">关于</a>

    </div>

    <div class="product">
        <div>
          <a  href="#/Chanpin" @click="msgs = 'one'"><img src="/one.png" alt="Power Fridge One"></a>
          <div class="nav-content-one-title">Power Fridge One</div>
        </div>
        
        <div>
          <a  href="#/Chanpin" @click="msgs = 'two'"><img src="/two.png" alt="Power Fridge two"></a>
          <div class="nav-content-one-title">Power Fridge Two</div>
        </div>
        
        <div>
          <a  href="#/Chanpin" @click="msgs = 'x'"><img src="/x.png" alt="Power Fridge x"></a>
          <div class="nav-content-one-title">Power Fridge X</div>
        </div>


        
    </div>

  </header>

  <main>
    
      <component :is="currentView" :msg="msgs"   @change="(msg) => msgs = msg"></component>
      
    
  </main>
  
  <footer>

  </footer>


</template>

<style scoped>

  .bg-black{
    transition: var(--transition-sd-03);
    position: absolute;
    background-color: rgba(0, 0, 0, 0.5);
    z-index: -1;
    opacity: 0;
    width: 100%;
    height: 100%;
    
  }

  

  .nav {
    transition:  var(--transition-sd-03);
    position: fixed;
    top: -80px;
    z-index: 99;
    width: 100%;
    height: 80px;
    background-color: rgb(255, 255, 255);
    
  }
  
  .nav-text{
    position: fixed;
    top: 0;
    width: 100%;
    padding: 20px 30px;
    
    z-index: 100;
    display: flex;
    justify-content: space-between;
  }

  .nav-text  a{
    transition: var(--transition-sd-02);
    color: rgb(255,255,255);
    cursor: var(--hover-pointer);
  }

  

  .product{
    transition: var(--transition-sd-03);
    position: fixed;
    left: 46.5%;
    width: 0;
    height: 0;
    background-color: rgb(255,255,255);
    opacity: 0;
    z-index: 101;
    display: grid;
    overflow-x: auto;
    padding: 50px 7.5% 0px;
    gap: 50px;
    grid-template-columns: repeat(7,1fr);
    grid-auto-rows: 200px;
  }

  

  .product > div {
    width: 130px;
    height: 80px;
  }

  .product > div img{
    width: 90%;
    transition: var(--transition-sd-03);
    border-radius: 8px;
    margin-bottom: 10px;
  }

  .product > div img:hover{
    transform: scale(1.1);
    cursor: var(--hover-pointer);
  }

  .product > div > div{
    transition: var(--transition-sd-02);
    font-size: 0.9rem;
  }

  .product > div > div:hover{
    cursor: var(--hover-pointer);
    color: var(--hover-color-green);
  }
</style>
