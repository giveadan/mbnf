<template>
  <div class="hero">
    <div class="flex" style="height:100%;">
      <div class="line" style="align-self:flex-end;" v-bind:class="{active: isActive}">
        <img class="fit" src="../assets/brad-dorris.png" />
      </div>
      <div class="flex-auto flexible-align">
        <h1>Brad - you may be married,<br>but you will not be forgotten.</h1>
      </div>
    </div>
  </div>
</template>


<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>
.hero {
  position: relative;
  width: 100%;
  background: #dbf5ff;
  height: 100vh;
}
img {
  vertical-align: text-bottom;
}

.flexible-align {
  align-self: center;
  text-align: center;
}

h1 {
  animation: fadein 1s 2s forwards;
  opacity:0;
/*  -moz-animation: fadein 5s;
  -webkit-animation: fadein 5s;
  -o-animation: fadein 5s; */
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

.line {
  animation: dash 3s ease-out forwards;
}

@keyframes dash {
  from {
    transform: translateX(-200px);
  }
  to {
    transform: translateX(0px);
  }
}

@media screen and (max-width: 560px) {
  h1 {
    font-size: 1.5em;
  }
  .flexible-align {
    position: absolute;
    top:0;
    padding:15px 10px;
  }
}

</style>
