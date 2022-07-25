<template>
    <div 
    className='bg-[#1AA37A] w-[90%] h-16 mt-28 mx-auto rounded-md flex justify-center 
    items-center transition-all ease-in-out hover:scale-105 md:hover:scale-[102%]
    md:h-24 md:w-[94%]
    '>
        <div className='flex' 
        v-for="feature in featuresList" :key="feature.id">
            <img :src="feature.imgSrc">
            <div class="textContainer">
                <h1 class="featureTitle">
                    {{feature.title}}
                </h1>
                <h1 class="featureContent">
                    {{feature.content}}
                </h1>
            </div>
        </div>

        


    </div>
</template>

<script>

export default {
   props:{
        featuresList:{
            type:Array,
            required:true,
        }
    },
}
</script>

<style>
.textContainer{
    @apply flex flex-col items-start justify-center
}
.featureTitle{
    @apply font-medium text-[0.36rem] sm:text-[0.8rem] md:text-[1.2rem]
}
.featureContent{
    @apply font-medium text-[0.27rem] text-[#004B35] sm:text-[0.50rem] md:text-[0.80rem]
}
img{
    @apply scale-50 sm:scale-[0.60] md:scale-[0.65]
}
</style>