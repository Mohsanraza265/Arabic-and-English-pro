<template>
    <div class="flex justify-between w-full items-center">
        <div>
            <h2 class=" text-[#282C41] dark:text-white text-[20px] font-semibold">{{name}}</h2>
            <p class="text-[#282C41] dark:text-white text-[14px] font-medium">{{ date }}</p>
        </div>
        <div>
            <p class="text-[#282C41] dark:text-white text-[20px] font-semibold">{{ plus }}</p>
        </div>

    </div>
</template>

<script setup>
    const props = defineProps({
        name: String,
        date: String,
        plus: String,
    });
</script>