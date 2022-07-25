<template>
    <div className="flex flex-col mx-5 gap-1 my-1 md:my-2">
        <h1 className='text-[0.6rem] md:text-[0.8rem]'>
            {{fieldName}}
        </h1>

        <input 
        :value="text"
        @input="updateInput"
        className='bg-[#505050] h-8 text-[0.6rem] w-60 
        rounded-sm pl-2 outline-none md:text-[0.8rem] lg:w-[36vw]
        '
        :placeholder="'Enter your '+ getFieldNameForPlaceholder">
    </div>
</template>
<script>
export default {
    props:{
        fieldName: String,
        text:String,
    },
    methods: {
        updateInput(event){
            this.$emit('update:text',event.target.value)
        }
    },
    computed:{
        getFieldNameForPlaceholder(){
            return this.fieldName.toLowerCase();
        }
    }
}
</script>
<style>
    
</style>