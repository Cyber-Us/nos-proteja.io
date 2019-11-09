<template>
  <section class="container-search">
    <div class="container">
      <h1>Verificar o status do site</h1>
      <h2>Trabalhando por uma Web mais segura</h2>
      <div class="box-search">
        <input
          class="search"
          type="text"
          placeholder="Pesquisar por URL"
          aria-labelledby="check-site-status"
        />
        <a href="#" class="hvr-sweep-to-right">Pesquisar</a>
      </div>
    </div>
    <div class="container-dog">
      <div class="dog">
        <div class="head">
          <div class="ears"></div>
          <div class="eyes"></div>
          <div class="beard">
            <div class="mouth">
              <div class="tongue"></div>
            </div>
          </div>
        </div>
        <div class="belt"></div>
        <div class="stomach"></div>
        <div class="legs">
          <div class="left"></div>
          <div class="right"></div>
        </div>
        <div class="tail"></div>
      </div>
      <h1 class="status"> Status </h1>
    </div>
    <footer>
      <div class="container result">Informações do site</div>
    </footer>
  </section>
</template>

<script>
export default {
  name: "Search"
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.negative .dog {
  position: fixed;
  left: 25%;
  top: 62%;
}
.negative .dog .mouth{
  height: 11px;
  margin: 8px auto 0px;
  border-radius: 0px 0px 0 0px;
}
.negative .dog .tail {
  bottom: -30px;
  -webkit-transform: rotate(109deg) translate(5px, 0px);
  transform: rotate(109deg) translate(5px, 0px);
}
.negative .dog .tongue{
  opacity: 0;
}
.positive .dog .tongue{
  animation: grow 0.1s infinite alternate;
}
.positive .dog .tail {
  transform: rotate(40deg) translate(5px, 0px);
  animation: shake 0.1s infinite alternate;
}
.negative .dog .belt{
  background-color: #333;
}
.positive h1, .positive h2,
.negative h1, .negative h2 {color:#FFF;}
.positive .search,.negative .search{
  background-color: #E57F38;
  border: 1px solid #E57F38;
}
.positive .hvr-sweep-to-right,
.negative .hvr-sweep-to-right{
  color:#FFF;
  background-color: #E57F38;
  border-radius: 6px;
}
.positive .hvr-sweep-to-right:before,
.negative .hvr-sweep-to-right:before{
   color:#333;
  background-color: #E57F38;;  
}
.container-dog{
    position: relative;  
    flex: 1;
}
.container-dog .status{
  display: block;
  position: absolute;
  top: 75px;
  left: 31px;
  text-align: center;
  font-size: 50px;
}
.container-dog:before {
  content: '';
  position: absolute;
  bottom: 13.3333333333%;
  left: 34%;
  display: block;
  width: 200px;
  height: 10px;
  bottom: -85px;
  background-color: #D3D1D1;
  border-radius: 2px;
  -webkit-animation: shadow calc(1 * var(calc(var(.7s) / 2))) infinite;
  animation: shadow calc(1 * var(calc(var(.7s) / 2))) infinite;
}
.container-search {
  align-items: center;
  display: flex;
  flex-direction: row-reverse;
  flex-wrap: wrap;
  justify-content: center;
  width: 100%;
  position: sticky;
  top: 3.75rem;
  padding: 10vh 0 0 0;
}
.container-search .container {
  flex: 1;
  width: 976px;
  margin: auto;
  color: #FFF;
  font-family: sans-serif;
  font-style: normal;
  font-weight: 900;
  text-align: left;
}
.container-search .container.result {
  background-color: #fff;
  height: 2px;
  opacity: 0;
}
.container-search .container.active {
  min-height: 300px;    
}
footer {
    -webkit-transition: all 0.3s ease;
    transition: all 0.3s ease;
    width: 100%;
    height: 0;
    margin: auto;
    margin: 15vh 0 0 0;
  }

h1 {
  font-size: 60px;
  line-height: 1;
  font-weight: 700;
  letter-spacing: -0.01em;
  text-align: left;
  margin: 10px 0;
  font-family: monospace;
  color:#4E8EDB;
  width: 90%;
}
h2 {
  font-weight: 100;
  font-size: 2em;
  font-family: monospace;
  color:#4E8EDB;
  text-align: left;
}
.search {
  display: block;
  width: 60%;
  height: 3.25rem;
  padding: 0 12px;
  font-size: 2rem;
  font-weight: 500;
  letter-spacing: 0.025em;
  color: #FFF;
  background-color: #4E8EDB;
  border: 1px solid #4E8EDB;
  border-radius: 6px;
  -webkit-transition: all 0.2s ease;
  transition: all 0.2s ease;
  outline: none;
  font-family: monospace;
}
.box-search{
  display: flex;
}
.hvr-sweep-to-right{
    text-decoration: none;
    padding: 10px;
    color: #FFF;
    background-color: #4E8EDB;
    font-size: 2rem;
    font-weight: 500;
    margin-left: 20px;
    font-family: monospace;
    line-height: 33px;
      border-radius: 6px;
}
.hvr-sweep-to-right:before{
  background-color: #E57F38; 
  border-radius: 6px; 
}
::-webkit-input-placeholder {
  color:#ffff; 
}

:-ms-input-placeholder {
  color:#ffff; 
}
::placeholder {
  color: #ffff; 
}

.dog{
    display: block;
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
}
.dog .head{
    display: block;
    width: 100%;
    height: 90px;
    border-radius: 40px 40px 0px 0px;
    position: absolute;
    left: 0px;
    bottom: 100%;
    background: #FFCC66;
}

.dog .ears{
  display: block;
  width: 100%;
  position: relative;
  z-index: -1;
}
.dog .ears::before {
  border-radius: 80px 20px 0px 0px;
  left: 0px;
  bottom: -40px;
  background: #FDD17B;
  transform: rotate(-59deg);
}
.dog .ears::after {
  right: 0px;
  bottom: -35px;
  border: 10px solid #FDD17B;
  border-radius: 20px 80px 0px 0px;
  background: #FFF2D8;
  transform: rotate(30deg);
}
.dog .ears::before, .dog .ears::after {
  content: "";
  width: 30px;
  height: 60px;
  box-sizing: border-box;
  position: absolute;
  transition: transform 0.5s ease;
}

.dog .ears:hover::before,
.dog .ears:hover::after{
  transform: none
}

.dog .eyes {
  display: block;
  width: 100%;
  margin: 15px 0px 6px;
  line-height: 1rem;
  text-align: center;
  position: relative;
}

.dog .eyes::before, .dog .eyes::after {
  content: "";
  display: inline-block;
  width: 10px;
  height: 10px;
  margin: 0px 12px;
  border-radius: 50%;
  background: #000;
  animation: squeeze 2s infinite;
}

.dog .beard {
    display: block;
    width: 40px;
    height: 40px;
    margin: 0px auto;
    border-radius: 5px 5px 15px 15px;
    background: #FFF2D8;
    position: relative;
}

.dog .beard::before {
    content: "";
    display: block;
    width: 20px;
    height: 10px;
    margin: 0px auto;
    border-radius: 0px 0px 10px 10px;
    background: #333;
}

.dog .mouth {
    display: block;
    width: 30px;
    height: 15px;
    margin: 5px auto 0px;
    border-radius: 0px 0px 15px 15px;
    background: #000;
    position: relative;
}

.dog .mouth::before {
    content: "";
    display: block;
    width: 100%;
    height: 3px;
    position: absolute;
    top: 0px;
    left: 0px;
    background: #FFF;
}
.dog .mouth:hover .mouth{
  height: 2px;
  border-radius: 0px 0px 15px 15px;
}
.dog .mouth:hover:hover .mouth::before{
  display: none;
}
.dog .tongue {
  display: block;
  width: 20px;
  height: 20px;
  margin-left: -10px;
  border-radius: 3px 3px 10px 10px;
  position: absolute;
  top: 7px;
  left: 50%;
  background: #900;
}
.dog .tongue:hover .tongue{
  height: 0px;
  animation: none;
}

.dog .belt {
  display: block;
  width: 104%;
  height: 20px;
  border-radius: 3px;
  background: #CC3300;
  position: relative;
  left: -2%;
  z-index: 3;
}

.dog .belt::before {
  content: "";
  display: block;
  width: 25px;
  height: 25px;
  margin-left: -12.5px;
  border-radius: 50%;
  position: absolute;
  top: 5px;
  left: 50%;
  background: #FFFFCC;
}

.dog .stomach {
    display: block;
    width: 100px;
    padding: 30px 0px 0px;
    background: #FFCC66;
    position: relative;
}

.dog .stomach::before {
    content: "";
    display: block;
    width: 50px;
    height: 100px;
    margin: 0px auto;
    border-radius: 25px 25px 0px 0px;
    background: #FFF2D8;
}
.dog .legs {
    display: block;
    position: relative;
}
.dog .legs::before {
    left: -16px;
    border-radius: 20px 0px 0px 0px;
}

.dog .legs::before, .dog .legs::after {
    content: "";
    display: block;
    width: 16px;
    height: 60px;
    background: #FCB449;
    position: absolute;
    bottom: 0px;
    z-index: 1;
}
.dog .legs .left, .dog .legs .right {
    display: block;
    width: 40px;
    height: 70px;
    position: absolute;
    bottom: 0px;
    z-index: 2;
}
.dog .legs .left {
    left: -20px;
}
.dog .legs .left::before {
    right: 0px;
}
.dog .legs .left::after {
    right: 15px;
}
.dog .legs .left::before, 
.dog .legs .right::before {
    width: 30px;
    height: 20px;
    background: #FFCC66;
    z-index: 2;
}
.dog .legs .left::before, 
.dog .legs .left::after, 
.dog .legs .right::before, 
.dog .legs .right::after {
    content: "";
    display: block;
    border-radius: 15px 15px 0px 0px;
    position: absolute;
    bottom: 0px;
}
.dog .legs .right {
    right: -20px;
}
.dog .legs .right::before {
    left: 0px;
}
.dog .legs .right::after {
    left: 15px;
}
.dog .legs::after {
    right: -16px;
    border-radius: 0px 20px 0px 0px;
}
.dog .tail {
  display: block;
  width: 50px;
  height: 120px;
  border-radius: 0px 100% 0px 0px;
  position: absolute;
  left: 100%;
  bottom: 20px;
  z-index: -1;
  transform: rotate(40deg) translate(5px, 0px);
}
.dog .tail::before {
    width: 60%;
    height: 80%;
    border-radius: 0px 100% 0px 0px;
    top: 0px;
}
.dog .tail::after {
    width: 75%;
    height: 60%;
    border-radius: 100% 0%;
    top: 30%;
}
.dog .tail::before, .dog .tail::after {
    content: "";
    display: block;
    position: absolute;
    left: 0px;
    background: #FFCC66;
}


@keyframes squeeze{
	90% {transform: none; animation-timing-function: ease-in;}
	93% {transform: scale(1.2, 0.3);}
	100%{animation-timing-function: ease-out;}		
}
@keyframes grow{
	0%{animation-timing-function: ease-in;}
	100%{height: 25px;}
}
@keyframes shake{
	0%{transform: rotate(40deg) translate(5px, 0px);}
	100%{transform: rotate(35deg) translate(0px, 0px);}
}
 @keyframes shadow {
      from, to {
        transform: scaleX(.75);
      }
      45%, 55% {
        transform: scaleX(.5);
      }
    }
</style>



