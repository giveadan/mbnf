<template>
  <div class="hero" id="test">
    <div class="flex" style="height:100%;">
      <transition name="fade">
        <div class="img-container" v-if="show">
          <img class="fit" src="../assets/brad-dorris.png" />
        </div>
      </transition>
      <div class="words flex-auto flexible-align">
        <h1>Brad - you were a great friend,<br>and I'll miss hanging out with you.</h1>
        <div class="content" @click="show = !show">
          <p v-if="show">Try to get a beer with Brad</p>
          <p v-else>Ask if he wants to go to Bed Bath & Beyond</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      show: true,
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss">

.content {
  padding: 0 8px;
  display:inline-block;
  background: #3B669E;
  color: white;
  border: 1px solid #ccc;
  border-radius: 10px;
  cursor: pointer;
}

.img-container {
  position: absolute;
  bottom: 0;
  left: 0;
  &.fade-enter-active:after {
    content: "Hell yeah! Let's Go!";
    position: absolute;
    top: 50%;
    right: -120px;
    width: auto;
    display: block;
    padding: 6px;
    border: 1px solid black;
    background: white;
  }
  &.fade-leave-active:after {
    content: "Can't. Sorry.";
    position: absolute;
    top: 50%;
    right: -100px;
    padding: 6px;
    border: 1px solid black;
    background: white;
    display: inline-block;
  }
}

.hero {
  position: relative;
  width: 100%;
  height: 100vh;
}
img {
  vertical-align: text-bottom;
}

.flexible-align {
  align-self: center;
  text-align: center;
}

.hero {
  animation: fadein .5s ease-in .5s forwards;
  opacity: 0;
}

@keyframes fadein {
    from { opacity:0;}
    to { opacity:1; }
}
@-moz-keyframes fadein { /* Firefox */
    from { opacity:0;}
    to { opacity:1; }
}
@-webkit-keyframes fadein { /* Safari and Chrome */
    from { opacity:0;}
    to { opacity:1; }
}
@-o-keyframes fadein { /* Opera */
    from { opacity:0;}
    to { opacity: 1; }
}


@keyframes dash {
  from {
    transform: translateX(-320px);
  }
  to {
    transform: translateX(0px);
  }
}

.fade-leave-active, .fade-enter-active {
  & + .words > .content {
    visibility: hidden;
  }
}

.fade-leave-active {
  animation: dash 2s linear forwards;
  animation-direction: reverse;
}

.fade-enter-active {
  animation: dash 2s ease-out forwards;
}


@media screen and (max-width: 560px) {
  h1 {
    font-size: 1em;
  }

  .content {
    font-size: 12px;
  }

  .flexible-align {
    position: absolute;
    top:0;
    width: 100%;
  }
}


</style>
