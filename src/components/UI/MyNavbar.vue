<template>
    <div 
    className="flex justify-end items-center 
    p-2 font-normal text-[0.6rem] gap-4 sm:text-[0.85rem] md:text-[1rem] ">
        <h1 className='text-[#1AA37A] font-bold text-base mr-auto cursor-default sm:text-xl md:text-2xl'>
            Brand®
        </h1>

        <h1 @click="this.$emit('scrollTo',aboutRef)"
            class="navbarLink">
            About us
        </h1>
        <MyButton @click="this.$emit('scrollTo',contactRef)">Contact us</MyButton>
    </div>
</template>

<script>
import MyButton from './MyButton.vue';
export default {
    components: { MyButton },
    data() {
        return {
            aboutRef: 'about',
            contactRef: 'contact',
        }
    },
}
</script>

<style>
.navbarLink{
    @apply text-[#B6B6B6] hover:scale-[1.06] cursor-pointer focus:scale-[1.06] active:scale-100 transition-all ease-in-out
}
</style>