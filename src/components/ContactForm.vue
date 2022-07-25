<template>
    <div 
    className='flex items-start justify-between flex-col w-[18rem] 
    sm:w-[18.4rem] h-80 bg-[#3F3F3F] rounded-md sm:ml-auto z-10
    text-[0.9rem] sm:mr-5 md:mr-10 md:w-[20rem] md:h-[21.5rem] lg:w-5/12 lg:mr-28
    '>

        <h1 className='mx-5 mt-1 font-bold text-[1.5rem]'>
            Register interest
        </h1>
        <h2 className='mx-5 text-[0.5rem] text-[#ACACAC] sm:text-[0.6rem] md:text-[0.7rem] lg:text-[0.8rem]'>
            Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vitae, in tristique senectus dui pharetra sit.
        </h2>

        <MyInput v-model:text="name" :fieldName="'Name'"></MyInput>
        <MyInput v-model:text="company" :fieldName="'Company'"></MyInput>
        <MyInput v-model:text="email"  :fieldName="'Email adress'"></MyInput>

        <MyButton id="button" @click="clearInputs">Submit</MyButton>
        
    </div>
</template>

<script>
import MyInput from './UI/MyInput.vue';
import MyButton from './UI/MyButton.vue';
export default {
    components: { MyInput, MyButton },
    data() {
        return {
            name: '',
            company: '',
            email: '',
        }
    },
    methods: {
        clearInputs(){
            this.name = ''
            this.company = ''
            this.email = ''
        }
    },
}
</script>

<style>
#button{
    margin-left: 1.25rem;
    margin-bottom: 1rem;
    scale: 0.80;
}
</style>