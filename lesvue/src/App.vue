<template>
  <div id="app">
    <h1>Список дел</h1>
    <hr>
    <router-view />
  </div>
</template>


<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.line{
   opacity: 0.5;
}
.showanimation {
  -webkit-animation: disappearance 4s linear;
          animation: disappearance 4s linear;
}
ul{
  padding-left: 0px;
}
@-webkit-keyframes disappearance {
  from {
    opacity: 1;
  }
  70% {
    opacity: 0.7;
  }
  50% {
    opacity: 0.5;
  }
  25% {
    opacity: 0;
  }
  to {
    opacity: 0;
  }
}

@keyframes disappearance {
  from {
    opacity: 1;
  }
  70% {
    opacity: 0.7;
  }
  50% {
    opacity: 0.5;
  }
  25% {
    opacity: 0;
  }
  to {
    opacity: 0;
  }
   }
.link-router{
  display: block;
  margin-bottom: 30px;
}
body {
  background: aliceblue;
}
.switch-sel{
  height: 30px;
    color: white;
    background: #007bff;
    border: none;
    padding: 0 5px;
    appearance: none;
  width: 160px;
    text-align: center;
    border-radius: 15px;
     font-size: 16px;
}
.switch-sel:focus{
  border:none;
  outline: none;
}
.switch-sel:active{
  border:none;
  outline: none;
}
.testselect{
border-radius: 15px 15px 0px 0px;
}
.create-task{
   margin: auto 0;
    border-radius: 20px;
    border: none;
    height: 38px;
    font-size: 16px;
    color: #fff;
    background: #007bff;
    padding-left: 20px;
   
}
.create-task:focus{
  border: none;
  outline: none;
}
.create-task-btn{
  width: 140px;
  height: 40px;
  font-size: 14px;
  font-weight: 600;
  color: #000;
  background-color: #fff;
  border: none;
  border-radius: 45px;
  box-shadow: 0px 8px 15px rgba(0, 0, 0, 0.1);
  transition: all 0.3s ease 0s;
  cursor: pointer;
  outline: none;
}
.create-task-btn:hover {
  background-color: #007bff;
  box-shadow: 0px 15px 20px #007bffab;
  color: #fff;
  transform: translateY(-7px);
}
input::-webkit-input-placeholder {
  color:#fff;
}
input:-moz-placeholder {
  color:#fff;
}
</style>
