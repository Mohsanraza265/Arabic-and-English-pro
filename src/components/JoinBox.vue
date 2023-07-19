<template>
    <div class="shadow p-4 bg-[#f6f5fe] dark:bg-[#282c41] rounded-lg">
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
            <p class="text-[#434344] dark:text-[#a0a9d8] text-[13px] font-medium ml-1 py-4"><i class="fa fa-arrow-right mr-1"></i> {{ date }} </p>
        </div>
        <div class="flex">
            <div>
                <button class=" text-white text-[13px] font-semibold bg-[#9484F7] border-0 py-1 px-4 focus:outline-none rounded text-lg "> Join </button>
            </div>
            <div>
                <button class="text-[#282C41] text-[13px] font-semibold dark:text-white border-0 py-1 px-4 focus:outline-none rounded text-lg"> Dismiss </button>
            </div>
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