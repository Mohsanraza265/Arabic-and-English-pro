<template>
    <div>
        <swiper 
            :slidesPerView="3" 
            :loop="true" 
            :spaceBetween="20" 
           
            :navigation="{ nextEl: '.next_btn', prevEl: '.prev_btn', }"
            :autoplay="{ delay: 5000, }" 
            :modules="modules" 
            class="mySwiper"
        >
            <swiper-slide v-for="text in swiperTextBase" :key="text.id" class=" py-2">
                <div class="bg-white dark:bg-slate-900 rounded-2xl border border-gray-300 hover:border-[#9484F7] shadow dark:border-white border-solid p-3 text-center">
                    <h1 class="text-[#282C41] dark:text-white text-[14px] hover:text-[#9484F7]">{{ text.day }}</h1>
                    <p class="text-[#282C41] dark:text-white text-[14px] hover:text-[#9484F7] bg-gray-300 dark:bg-[#9484F7] rounded-2xl w-[30px] mx-auto">{{ text.number }}</p>
                    
                </div>
            </swiper-slide>
        </swiper>
        
    </div>
</template>
<script>
import { Swiper, SwiperSlide } from 'swiper/vue';
// Import Swiper styles
import 'swiper/css';

import 'swiper/css/pagination';



// import required modules
import { Autoplay, Pagination } from 'swiper/modules';
import { Navigation } from 'swiper';

import { ref, reactive } from 'vue'
export default {
    components: {
        Swiper,
        SwiperSlide,
    },
    setup() {
        const swiperTextBase = ref([
            {
                day: 'Today',
                number: 25,
                id: 1
            },
            {
                day: 'Monday',
                number: 25,
                id: 2
            },
            {
                day: 'Tue',
                number: 25,
                id: 3
            },
            {
                day: 'Wed',
                number: 25,
                id: 4
            },
            {
                day: 'Thur',
                number: 25,
                id: 5
            },
            {
                day: 'Fri',
                number: 25,
                id: 6
            },
            {
                day: 'Satur',
                number: 25,
                id: 7
            },
        ]);
        return { modules: [Pagination, Autoplay], swiperTextBase }
    }
}

</script>

