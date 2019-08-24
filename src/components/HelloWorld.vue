<template>
  <div class="pin-home">
  <div class="up">
    <div class="pin"><i class="fa fa-sort-desc" aria-hidden="true"></i></div>
      <div class="pin-text">Enter your PIN code</div>
      <div class="pin-text-second-line">To confirm your departure</div>
      <div class="input">
        <input value="7"/>
        <input value="0"/>
        <input/>
        <input/>
      </div>
  </div>  
    <div class="down">
      <div class="numbers">
          <div class="num">1</div>
          <div class="num">2</div>
          <div class="num">3</div>
          <div class="num">4</div>
          <div class="num">5</div>
          <div class="num">6</div>
          <div class="num">7</div>
          <div class="num">8</div>
          <div class="num">9</div>
          <div class="num">x</div>
          <div class="num">0</div>
          <div class="num"><i class="fa fa-window-close" aria-hidden="true"></i></div>
      </div>
      </div>  
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="css">
@import 'https://stackpath.bootstrapcdn.com/font-awesome/4.7.0/css/font-awesome.min.css'; 

.up{
  background-color: #8656C4;
  height:200px;
  width: 215px;
  border-radius: 7px 7px 0px 0px;
}
.down{
    background-color: #FFFFFF;
  height:190px;
  width: 215px;
      border-radius: 7px 7px 0px 0px;
      margin-top: -5px;
}

.pin{
  color: #FFFFFF;
  /* transform: rotate(180deg); */
  float: left;
    padding: 12px;
}

.pin-text{
  color: #FFFFFF;
  font-weight: bold;
  margin-top: 50px;
    margin-left: 12px;
    position: absolute;
        font-size: 15px;
}

.pin-text-second-line{
  color: #FFFFFF;
  font-size: 10px;
    margin-top: 70px;
    margin-left: 12px;
    position: absolute;

}
input{
          width: 35px;
      margin-left: 10px;  
        background-color: #8656C4;
        border-color: transparent;
         border: none;
         color: #fff;
         border-bottom: 2px solid #A56BEF;
         font-size: 22px;
         text-align: center;
}

input:focus{
    outline: none;
    background-color: #8656C4;
}
.input{
 margin-top: 125px;
    margin-left: 12px;
    position: absolute;
}
.numbers{
  display: grid;
    grid-template-columns: auto auto auto;
    padding: 10px;
    border-radius: 10px;
}
.num{
color: #676767;
    border: 1px solid #fff;
    padding: 10px;
    font-size: 15px;
    text-align: center;
}

</style>
