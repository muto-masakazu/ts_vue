<template>
  <div class="container">
    <div class="links">
      <router-link to="/about"><img src="/image/omega.png"></router-link>
     </div>
    <div class="left-side">
      <div id="rei">
        <img @mousemove="onMouse" @mouseout="onStop" src="/image/rei_full.png">
      </div>
    </div>
    <div class="right-side">
      
      <img src="/image/rio_full.png">
    </div>
  </div>
</template>

<script lang="ts">
import { Component, Vue, Prop } from 'vue-property-decorator';
import HelloWorld from '@/components/HelloWorld.vue'; // @ is an alias to /src

@Component({
  components: {
    HelloWorld,
  },
})

export default class Home extends Vue {
  onMouse(e){
    //let element = document.getElementsByClassName('rei');
    /*let element = document.getElementById('rei');
    let ax = -(window.innerWidth / 2 - e.pageX) / 10;
    let ay = (window.innerHeight / 2 - e.pageY) / 5;
    element.setAttribute("style", "transform: rotateY("+ax+"deg) rotateX("+ay+"deg);-webkit-transform: rotateY("+ax+"deg) rotateX("+ay+"deg);-moz-transform: rotateY("+ax+"deg) rotateX("+ay+"deg)");
  */
  }
  onStop(){
    //let element = document.getElementById('rei');
    //element.setAttribute("style", "transition:.2s;transform: rotateY(0deg) rotateX(0deg);-webkit-transform: rotateY(0deg) rotateX(0deg);-moz-transform: rotateY(0deg) rotateX(0deg)");
  }
}
</script>

<style lang="scss">
.container {
  height: 100vh;
  display: flex;
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  -webkit-transition: .5s ease;
  transition: .5s ease;
  opacity: 1;
  .links{
    position: absolute;
    top: 40%;
    left: 50%;
    transform: translate(-50%, -50%);
    img{
      height: 30%;
      width: 30%;
      opacity: 1;
      -webkit-transition: .3s ease-in-out;
      transition: .3s ease-in-out;
      &:hover{
        width: 40%;
        height: auto;
        -webkit-transition: .3s ease-in-out;
        transition: .3s ease-in-out;
        opacity: .5;
      }
    }
  }
  img{margin-top: 15%;}
}
.left-side{
  height: 100vh;
  flex-basis: 50%;
  background-color: rgba($color: #000, $alpha: 0.6);
  img{
    -moz-user-select: none; /* Firefox */
    -ms-user-select: none; /* Internet Explorer */
    -khtml-user-select: none; /* KHTML browsers (e.g. Konqueror) */
    -webkit-user-select: none; /* Chrome, Safari, and Opera */
    -webkit-touch-callout: none; /* Disable Android and iOS callouts*/
    transition: 1s;
    &:hover{
      transform: rotateY(360deg);
    }
  }
  
}
.right-side{
  height: 100vh;
  flex-basis: 50%;
  background-color: rgba($color: #000, $alpha: 0.6);
  img{
    -webkit-transition: .8s ease-in-out;
    transition: 1s ease-in-out;
    opacity: 1;
    &:hover{
      -webkit-transition: .8s ease;
      transition: .8s ease-in-out;
      opacity: .1;
}
  }
}
</style>
