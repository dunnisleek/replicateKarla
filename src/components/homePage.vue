<template>
  <div class="container">
  <div class="wrapper">
    <div class="column contentbox">
      <h1>MOBILE POS</h1>
      <h2>Contactless payments built for Africa.</h2>
      <p>We are building a platform that truly enables businesses go mobile by empowering them with tools to 
        collect local / international payments, manage transactions, teams, and so much more.</p>

        <form>
          <input type="text" placeholder="Email Address" required/>
          <button>Get Early Access</button>
        </form>

      <div class="footerBtn" @click="showMe">learn about the team <span><img src="../assets/download.svg"/></span></div>
    </div>
    <div class="column rightimg">
      <img src="../assets/hero-bg.023af3b.png"/>
    </div>
 
  </div>
</div>
<div v-show="display">
  <vision-nee @close-vision-page="hideVisionPage"></vision-nee>
</div>
</template>

<script>
import visionNee from './visionNee.vue';
  export default {
    components:{
      visionNee
    },
    data(){
      return{
        display:false
      }
    },
    methods:{
      showMe(){
        this.display = true
    },
    hideVisionPage() {
      this.display = false;
    }
  
    }
  }
</script>

<style scoped>
  .container{
   /* max-width: 1400px; */
   border:5px solid white;
   margin: auto;
   margin-top:10px;
  }
 .wrapper{
  /* margin: 0 auto; */
  background: #FEF1E0;
  display:flex;
  justify-content: space-between;
  
  border-radius: 30px;
  align-items: center;
  gap:60px;
  height:90vh;
  padding:2rem 1rem; 
  
 }

 .rightimg{
  flex:1;
 }
 .rightimg img{
  width:95%;
  position: relative;
  left:35px;
  /* height:70%; */
 }
 .contentbox{
  
    width: 35%;
    padding-left: 120px;
}
 .contentbox h2{
  font-size:45px;
  line-height: 48px;
  color:#00140b;
 }
 .contentbox h1{
  font-size:16px;
  line-height: 22px;
  Color:#014223;
 }
 .contentbox p{
  width:450px;
  font-size:18px;
  line-height: 22px;
 }
/* footer button */
.footerBtn{
  position: absolute;
  /* top:0; */
  bottom: 0;
  color:#e78400;
  font-family: 'Titillium Web', sans-serif;
  font-size:14px;
  line-height: 21px;
  text-transform: uppercase;
  font-weight: 700;
  padding-bottom: 20px;
  cursor: pointer;
  transition: all 0.3s ease-in-out;
}
.footerBtn:hover{
  transform:scale(1.1);
}
.footerBtn span{
  padding-left:10px;

}

/* FORM STYLE */
form button{
  font-size:14px;
  font-family: 'Titillium Web', sans-serif;
  font-weight: 600;
  line-height: 22px;
  text-transform: uppercase;
  background:#e78400;
  padding:17px;
  color:#fff;
  border:none;
  border-radius:10rem;
  position: relative;
  top:5.5px;
  left:20rem;
  cursor: pointer;
  transition: all 0.3s ease-in-out;
}
form button:hover{
  transform: scale(1.1);
}
form input{
  font-family: 'Titillium Web', sans-serif;
  font-weight: 600;
  padding:24px;
  width:430px;
  position: absolute;
  border-radius:10rem;
  border:none;
Color:#66687e;
outline:none;
}
</style>