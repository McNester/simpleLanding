<template>
<button 
    className='rounded-3xl w-[5rem] h-7 bg-[#1AA37A] text-white font-bold 
    shadow-[rgb(157,255,179,0.20)] shadow-[0px_0px_10px_2px] 
    hover:scale-[1.06] focus:font-medium active:scale-100 
    hover:shadow-[0px_0px_20px_2px] hover:shadow-[rgb(157,255,179,0.20)]
    transition-all ease-in-out sm:w-[6rem]
    sm:shadow-[rgb(157,255,179,0.20)] sm:shadow-[0px_0px_20px_3px] 
    sm:hover:shadow-[0px_0px_30px_3px] sm:hover:shadow-[rgb(157,255,179,0.20)]
    md:w-[8rem]'
    >
        <slot></slot>
</button>
</template>
<script>
export default {
    
}
</script>
<style>
    
</style>