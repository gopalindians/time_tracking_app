<template>
  <div class="pin-home">
  <div class="up">
    <div class="pin"><i class="fa fa-sort-desc" aria-hidden="true"></i></div>
      <div class="pin-text">Enter your PIN code</div>
      <div class="pin-text-second-line">To confirm your departure</div>
      <div class="input">
        <input maxlength="1" v-model="pinVal1" @focus="focused(1)"/>
        <input maxlength="1" v-model="pinVal2" @focus="focused(2)"/>
        <input                maxlength="1" v-model="pinVal3"  @focus="focused(3)"/>
        <input                 maxlength="1" v-model="pinVal4"  @focus="focused(4)"/>
      </div>
  </div>  
    <div class="down">
      <div class="numbers">
          <div class="num" @click="handleNumClick(1)">1</div>
          <div class="num" @click="handleNumClick(2)">2</div>
          <div class="num" @click="handleNumClick(3)">3</div>
          <div class="num" @click="handleNumClick(4)">4</div>
          <div class="num" @click="handleNumClick(5)">5</div>
          <div class="num" @click="handleNumClick(6)">6</div>
          <div class="num" @click="handleNumClick(7)">7</div>
          <div class="num" @click="handleNumClick(8)">8</div>
          <div class="num" @click="handleNumClick(9)">9</div>
          <div class="num" @click="handleNumClick('x')">x</div>
          <div class="num" @click="handleNumClick(0)">0</div>
          <div class="num" @click="handleNumClick('CLEAR')"><i class="fa fa-window-close" aria-hidden="true"></i></div>
      </div>
      </div>  
  </div>
</template>

<script>
export default {
  name: 'Pin',
  props: {
    msg: String
  },
  data(){
    return{
    pinVal1:7,
    pinVal2:0,
    pinVal3:'',
    pinVal4:'',
    pinPlace:0
    }
  },

  methods:{
    handleNumClick(num){
      if(num=='CLEAR'){
        this.pinVal1='';
        this.pinVal2='';
        this.pinVal3='';
        this.pinVal4='';
      }else if (num=='x'){
        if(this.pinPlace==1){
          this.pinVal1='';
        }else if(this.pinPlace==2){
          this.pinVal2='';
        }else if(this.pinPlace==3){
          this.pinVal3='';
        }else{
        this.pinVal4='';
      }
      }else{
        if(this.pinPlace==1){
          this.pinVal1=num;
        }else if(this.pinPlace==2){
          this.pinVal2=num;
        }else if(this.pinPlace==3){
          this.pinVal3=num;
        }else{
        this.pinVal4=num;
      }
      }
      },
      focused(pinPlace){
        this.pinPlace=pinPlace;
      }
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

.num:active{
  background-color: #ECDFF6;
  color: #8D58B5;
}

</style>
