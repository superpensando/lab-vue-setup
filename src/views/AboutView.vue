<template>
  <h1 class="about-me__title">About me</h1>
  <div class="about-me__body">
    <p>Hello! My name is <span>{{name}} {{surname}}</span></p>
    <p>You have more information about me clicking my Social Networks!</p>
    <p class="about-me__social-networks">
      <span @click="helloWorld('Twitter')">Twitter</span> | <span @click="helloWorld('Linkedin')">Linkedin</span> 
      <br/>
      <a v-show="url" :href="url" :title="urlName" target="_blank">{{url }}</a>
    </p>
  </div>

</template>

<script>
export default {
  data() {
    return {
      name: "Laura",
      surname:"Rodríguez Castillo",
      url:"",
      urlName:"",   
    }
  },
  methods: {
    helloWorld(redSocialNetwork){
      console.log(redSocialNetwork);
      if (redSocialNetwork ==="Twitter") {
        this.url="http://twitter.com/superpensando",
        this.urlName="Twitter"
      } else {
        this.url= "https://es.linkedin.com/in/laurarodriguezcastillo",
        this.urlName= "Linkedin"
      }
  }
}
}
</script>

<style lang="scss">
.about-me__title {
  font-weight:bold;
  color: green;
}
.about-me__body {
  max-width:500px;
  margin: 0 auto;
  padding:50px;
  .about-me__social-networks {
    span {
        cursor:pointer;
        margin:0 10px;
        font-weight: bold;
    }
 
  }
  a {
    text-decoration: none;
    display:block;
    margin:20px auto;
    padding:20px; 
    color:white;
    background-color: green;
    &:hover {
      font-size:102%;
    }
  }
}



</style>
