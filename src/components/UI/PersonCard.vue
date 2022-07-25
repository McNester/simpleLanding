<template>
    <div 
    className='flex items-center justify-start w-[45%] 
    p-[0.20rem] rounded-lg bg-[#3F3F3F] mt-5
    hover:scale-[1.04] transition-all ease-in-out
    cursor-default sm:w-[60%] md:w-[68%] lg:w-[75%]
    '>
        <img
             :src="getSrcImage" className='scale-[0.70] md:scale-[0.80] lg:scale-[0.82]'>
        <div className='flex flex-col justify-start items-start h-full text-[0.4rem]'>
            <h1 className='text-white sm:text-[0.65rem] md:text-[0.80rem]'>
                {{personsInf.name}}
            </h1>
            <h1 className='text-[#ACACAC] sm:text-[0.65rem] md:text-[0.80rem]'>
                {{personsInf.comment}}
            </h1>

        </div>
    </div>
</template>

<script>
export default {
    
    props:{
        personsInf: {
            type: Object,
            required: true,
        }
    },
    computed:{
        getSrcImage(){
            console.log(this.personsInf.srcImg)
            return this.personsInf.srcImg
        }
    }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;500;700&display=swap');

*{
    font-family: 'Inter', sans-serif;
    font-weight: 500;
}
</style>