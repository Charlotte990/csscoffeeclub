<template>
  <div class="topone">
    <div id="circle">
    </div>
  </div>
</template>

<style>

#circle {
  background: #cfe7f0;
  width: 200px;
  height: 200px;
  border-radius: 50%;
  text-align: center;
  margin: 0 auto;
  animation: bounceIn 2s;
  animation-iteration-count: 2;
  opacity: 0;
}

#circle:hover {
  animation-play-state: paused;
}

@keyframes bounceIn {
  0% {
    transform: scale(0.1);
    opacity: 0;
  }
  60% {
    transform: scale(1.2);
    background: #9FCFE1;
    opacity: 1;
  }

  100% {
    transform: scale(0.1);
    opacity: 0.5;
  }
}
</style>
