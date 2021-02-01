<template>
  <div id="app">
    <h1>{{msg}}</h1>
<div class="portfolioContainer">
<div v-for="(mm , index) in m" class="ImageCol">
<div class="portfolioContent">
<h3> {{ index }}. {{ mm.dividends }} ÷ {{ mm.divisors }} =</h3>
<p> 
</p>
</div>
</div>
</div>

</div>
</template>

<script>
const ms = [];
for (var i = 0; i < 20; i++){
  var dividend =  Math.floor((Math.random() * 999) + 1);
  var divisor = Math.floor((Math.random() * 299) + 1);
  ms.push({dividends : dividend,
    divisors : divisor,
    quotients : Math.floor(dividend / divisor),
    remainders : dividend % divisor 
  });
}


export default {
  name: 'App',
  data () {
    return {
      msg:"division practice for grades 3 at TianMu elementary school!",
      m:ms
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;

}
* {
box-sizing: border-box;
}

h1 {
font-size: 30px;
text-align: center;
font-family: monospace, serif, sans-serif;
}

body {
background-color: #f1f1f1;
padding: 5px;
font-family: Arial;
}
main {
max-width: 1000px;
margin: auto;
}
.portfolioContainer {
margin: 8px -16px;
}
.portfolioContainer,
.portfolioContainer > .ImageCol {
padding: 0px;
}
.ImageCol {
float: left;
width: 25%;
height: 165px;
}
.portfolioContainer:after {
content: "";
display: table;
clear: both;
}
.portfolioContent {
float: left;
padding: 10px;
}
@media screen and (max-width: 900px) {
.ImageCol {
width: 50%;
}
}
@media screen and (max-width: 600px) {
.ImageCol {
width: 100%;
}
}


</style>
