<template>
    <div className="flex flex-col justify-center items-center mt-10">

        <div className='flex flex-col justify-center items-center h-20'>
            <h1 className='font-bold md:text-2xl'>Trusted by</h1>
            <img src="/imgSrc/trustedLine.png" className='md:scale-[0.8]'>
            <h2 className='font-medium text-[0.5rem] w-1/2 text-center text-[#ACACAC] mt-1 md:w-10/12 md:text-[0.75rem]'>
                Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vitae, in tristique senectus dui pharetra sit.
            </h2>

        </div>
        
        <div className='flex justify-center items-center scale-75 w-1/2 md:scale-90'>
            <img class="logo" src='/imgSrc/microsoft.svg'>
            <img class="logo" src='/imgSrc/tweeter.svg'>
            <img class="logo" src='/imgSrc/cocacola.svg'>
        </div>
        
    </div>
</template>

<script>
export default {
    
}
</script>

<style>
.logo{
    @apply transition-all ease-in-out hover:scale-[0.60] md:hover:scale-[0.8]
}
    
</style>