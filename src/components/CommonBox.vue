<template>
    <div class="shadow my-4 p-4 bg-white dark:bg-[#282c41] rounded-lg">
        <div class="flex items-center ">
            <div>
                <img :src="require(`../assets/${imgUrl}.png`)" class=" w-auto mr-3" alt="Img">
            </div>
            <div>
                <h2 class=" text-[#282C41] dark:text-white text-[15px] font-bold "> {{ title }}</h2>
                <p class="text-[#282C41] dark:text-white text-[13px] font-medium"> {{ para }} </p>
            </div>
        </div>
        <div>
            <p class="text-[#434344] dark:text-[#a0a9d8] text-[13px] font-medium ml-1 pt-4"><i class="fa fa-arrow-right mr-1"></i> {{ date }} </p>
        </div>
        
    </div>
</template>


<script setup>
const props = defineProps({
        title: String,
        imgUrl: String,
        date: String,
        para: String,
    });


// const props = defineProps({
//   product: Object
// })

// console.log(props.imgUrl, "test")
    

</script>