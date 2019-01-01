<template>
  <div class="about">
    <!--<div class="is-harf">
      <h1>ABOUT</h1>
    </div>
    <div class="is-harf">
      <h1>This is an about page</h1>
          <router-link to="/">TOP</router-link>
    </div>-->
    <svg>
      <text x="0" y="100%">Omesis is Good.</text>
    </svg>
    <!--<svg class="intro" viewbox="0 0 200 86">
      <text text-anchor="start" x="10" y="30" class="text text-stroke" clip-path="url(#text1)">Omesis</text>
      <text text-anchor="start" x="10" y="50" class="text text-stroke" clip-path="url(#text2)">is</text>
      <text text-anchor="start" x="10" y="70" class="text text-stroke" clip-path="url(#text3)">Good.</text>
      <text text-anchor="start" x="10" y="30" class="text text-stroke text-stroke-2" clip-path="url(#text1)">Omesis</text>
      <text text-anchor="start" x="10" y="50" class="text text-stroke text-stroke-2" clip-path="url(#text2)">is</text>
      <text text-anchor="start" x="10" y="70" class="text text-stroke text-stroke-2" clip-path="url(#text3)">Good.</text>
      <defs>
        <clipPath id="text1">
          <text text-anchor="start" x="10" y="30" class="text">Omesis</text>
        </clipPath>
        <clipPath id="text2">
          <text text-anchor="start" x="10" y="50" class="text">is</text>
        </clipPath>
        <clipPath id="text3">
          <text text-anchor="start" x="10" y="70" class="text">Good.</text>
        </clipPath>
      </defs>
      <path d="M70.598,16.753c-1.722-1.24-4.113-0.852-5.349,0.866c-1.242,1.716-0.853,4.113,0.865,5.35   c13.613,9.818,18.021,27.857,10.482,42.89c-4.082,8.138-11.088,14.202-19.726,17.066c-8.636,2.871-17.877,2.2-26.013-1.879   c-8.134-4.083-14.197-11.088-17.066-19.722c-2.866-8.642-2.197-17.877,1.886-26.014c4.958-9.89,14.458-16.779,25.413-18.429   c0.074-0.008,0.137-0.036,0.211-0.053l0.157,7.571c0.021,0.839,0.542,1.585,1.321,1.889c0.782,0.305,1.672,0.11,2.25-0.496   l10.904-11.379c0.794-0.828,0.764-2.142-0.062-2.933L44.492,0.577c-0.606-0.582-1.499-0.739-2.267-0.399   c-0.251,0.108-0.476,0.269-0.662,0.462c-0.372,0.389-0.585,0.919-0.579,1.479l0.151,7.212c-0.385-0.063-0.78-0.087-1.188-0.027   c-13.418,2.021-25.052,10.46-31.125,22.571C-1.499,52.451,6.85,77.584,27.424,87.901c5.989,3.005,12.362,4.429,18.646,4.429   c15.306,0,30.065-8.439,37.382-23.028C92.688,50.884,87.284,28.782,70.598,16.753z" fill="#404853"/>
    </svg>-->
  </div>
</template>
<script lang="ts">
import Vue from 'vue'
export default Vue.extend({})
</script>

<style lang="scss">
.about{
  height:100vh;
  display: flex;
  background-color: rgba($color: #000, $alpha: 0.0);
  .is-harf{
    flex-basis: 50%;
  }
}

svg{
  position: absolute;
  width: 900px;
  top: 30%;
  left: 25%;
}
text {
    /* 色はお好みで */
    stroke: black;
    /* 色はお好みで */
    fill: white;
    /* 文字が大きい方がアニメーションが綺麗なので50pxを指定 */
    font-size: 100px;
    /* 100%だと最後まで表示されないので多めに設定する */
    stroke-dasharray: 150% 150%;
    /* 線が細いほうがアニメーションが綺麗なので0.5pxを指定 */
    stroke-width: 0.5px;
    -webkit-animation: stroke-anim 10s linear;
    animation: stroke-anim 10s linear;
}
@-webkit-keyframes stroke-anim {
  0% {
    /* 100%だと最後まで表示されないので多めに設定する */
    stroke-dashoffset: 150%;
    fill:transparent;
  }
  50% {
    fill:transparent;
  }
  100% {
    stroke-dashoffset: 0%;
    fill:white;
  }
}

@keyframes stroke-anim {
  0% {
    /* 100%だと最後まで表示されないので多めに設定する */
    stroke-dashoffset: 150%;
    fill:transparent;
  }
  50% {
    fill:transparent;
  }
  100% {
    stroke-dashoffset: 0%;
    fill:white;
  }
}
/*svg.intro {
  max-width: 800px;
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  box-shadow: 0 30px 50px -20px rgb(46, 6, 66);
  .text { 
    display: none;
  }
  &.go {
    .text {
      font-family: Arial, sans-serif;
      font-size: 20px;
      text-transform: uppercase;
      display: block;
    }
    .text-stroke {
      fill: none;
      stroke: #51256f;
      stroke-width: 2.8px;
      stroke-dashoffset: -900;
      stroke-dasharray: 900;
      stroke-linecap: butt;
      stroke-linejoin: round;
      animation: dash 2.5s ease-in-out forwards;
    }
    .text-stroke:nth-child(2) {
      animation-delay: .3s;
    }
    .text-stroke:nth-child(3) {
      animation-delay: .9s;
    }
    .text-stroke-2 {
      stroke: #f6bdfa;
      animation-delay: 1.2s;
    }
    .text-stroke:nth-child(5) {
      animation-delay: 1.5s;
    }
    .text-stroke:nth-child(6) {
      animation-delay: 1.8s;
    }
  }
}*/

@keyframes dash {
  100% {
    stroke-dashoffset: 0;
  }
}
</style>

