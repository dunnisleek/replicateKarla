<template>
 <div class="main-container">
  <div class="founder-section">
    <header>
     
      <img
      @click="closeVisionPage"
       class="close"
        src="../assets/modal-close.svg"
        width="10"/>

      <h1>Meet the chief Visioneer</h1>
    </header>
    <div class="wrap">
      <img class="found" src="../assets/founder.560d257.png" />
      <h2>Ayo Onasanya</h2>
      <p class="cofounder">Co-Founder</p>
      <p class="para">
        Ayo has been helping companies plan, design and develop their digital
        products for over ten years. He has served in various capacity for
        early-stage startups, as well as enterprise and publicly traded
        companies.
      </p>
      <ul class="experience">
        <li>. 9+ years Fintech Experience</li>
        <li>. Repeat Founder</li>
        <li>. Bootstrapped from $0 to $50k/MRR in 2 years</li>
      </ul>
      <div class="social">
       <a :href="linkInLink">
       <img src="../assets/linkedin-logo.svg"/>
       </a>
      </div>
    </div>
  </div>
</div>
</template>

<script>
export default {
       data(){
              return{
               linkInLink:"https://www.linkedin.com/in/ayomideonasanya/"
              }
       },
  methods: {
       closeVisionPage() {
       this.$emit('close-vision-page')
    }
  },
};
</script>

<style scoped>

.founder-section {
  background:#FEF1E0;
  width: 700px;
  max-width: 700px;
  display: flex;
  flex-direction: column;
  align-items: center;
  border-radius: 3rem 0rem 0rem 3rem;
  padding-top: 1rem;
  position: relative; 
  top: 0;
  right: 0;
  bottom: 0;
  transition: transform 0.3s ease-in-out;
}
/* THIS IS WRAPPER FOR ALL CONTAINER */
.main-container{
    background: rgba(0,0,0,.5);
    width:100%;
    display: flex;
    justify-content: flex-end;
    position: absolute;
    top: 0;
  right: 0;
  bottom: 0;

}
.found {
  width: 80px;
}
/* THIS IS WHAT WRAP FROM THE IMAGE DOWNWARD */
.wrap {
  width: 500px;
  text-align: center;
  padding-top:2rem;
}
.wrap h2{
 font-size:16px;
 line-height:22px;
}
.para{
       max-width:430px;
       margin:0 auto;

}
.cofounder{
       margin-top: -0.7rem;
}
/* end of wrap text*/

/* CLOSE BUTTON */
.close {
  width: 25px;
  cursor:pointer;
  position: absolute;
  left: 40px;
}
header {
  display: flex;
  justify-content: space-between;
  align-items: center;
}
header h1 {
  font-size: 24px;
  font-family: "Titillium Web", sans-serif;
  font-weight: 400;
}

/* EXPERIENCE BULLETPOINT */
.experience li{
       color:#66687e;
       padding-bottom:10px;
       text-align: center;
       
}
ul{
       list-style-type: none;
}
</style>
