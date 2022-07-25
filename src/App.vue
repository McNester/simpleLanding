<template>
  <div id="app" className=' w-screen bg-background bg-center bg-cover overflow-hidden'>
    <MyNavbar @scrollTo="goToSection"></MyNavbar>
    
    <div ref="about" className='flex justify-center items-center w-screen relative sm:justify-between'>

      <div className='flex flex-col pt-5 pl-5 z-10'>
        <h1 className=' text-2xl md:text-4xl'>
          Lorem ipsum 
          <div className='text-[#1AA37A] inline-table'>
            brand
            <img src="/imgSrc/brandLine.svg" className='scale-50 origin-left absolute md:scale-[0.75]'>
          </div>
          sit <br>amet yo 👋
        </h1>

        <PersonCard v-for="person in peopleForCard" :key="person.id" :personsInf="person">
          <img src="imgSrc/firstPerson.png">
        </PersonCard>

      </div>

      <img src="/imgSrc/backImg.png" className="scale-[0.52] absolute origin-right right-2 mt-7 sm:-right-4 md:-right-4 lg:scale-[0.59] lg:right-5">


    </div>

    <FeaturesList :featuresList="this.featuresList"></FeaturesList>

    <Trusted></Trusted>

    <div ref="contact" className='flex justify-center items-center w-screen px-2 h-80 relative'>
        <img src="/imgSrc/secondBackImg.png"  className="scale-[0.50] absolute origin-left left-0 hidden sm:block ml-10 md:scale-[0.55] lg:ml-28 ">
        <ContactForm></ContactForm>
    </div>

    <div className="w-screen h-[0.01rem] bg-[#ACACAC] mt-7 absolute"></div>
    <MyNavbar @scrollTo="goToSection" id="footer"></MyNavbar>
    

    
  </div>
</template>


<script >
import smoothscroll from 'smoothscroll-polyfill';

import PersonCard from "./components/UI/PersonCard.vue";
import MyNavbar from "./components/UI/MyNavbar.vue";
import FeaturesList from "./components/FeaturesList.vue";
import Trusted from "./components/Trusted.vue";
import ContactForm from "./components/ContactForm.vue";

export default{
  
  components: { PersonCard, MyNavbar, FeaturesList, Trusted, ContactForm },
  data() {
    return {
      peopleForCard:[
        {id:0,name:'Lara Lin',comment:'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vitae, in tristique senectus dui pharetra sit.'},
        {id:1,name:'Andrew Reed',comment:'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vitae, in tristique senectus dui pharetra sit.'},
        {id:2,name:'Crista Anderson',comment:'Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vitae, in tristique senectus dui pharetra sit.'},
      ],
      featuresList:[
        {id:0,title:'24/7 support',content:'Lorem ipsum dolor sit amet, consectetur adipiscing elit',imgSrc:'/imgSrc/lock.png'},
        {id:1,title:'1000+ of reviews',content:'Lorem ipsum dolor sit amet, consectetur adipiscing elit',imgSrc:'/imgSrc/graphic.png'},
        {id:2,title:'And more!',content:'Lorem ipsum dolor sit amet, consectetur adipiscing elit',imgSrc:'/imgSrc/trophy.png'}
      ]
    }
  },
  methods:{
      goToSection(sectionRef){
        var element = this.$refs[sectionRef]
        var elTop = element.offsetTop

        smoothscroll.polyfill();
        window.scrollTo({top:elTop,behavior: 'smooth'})

    }
  }
}


</script>

<style>
*{
    font-family: 'Inter', sans-serif;
    color: white;
}
#footer{
  @apply mt-10
}
</style>
