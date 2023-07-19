<template>
  <div class=" bg-[#e9eaf2] dark:bg-slate-900 h-screen">
    <div class=" container mx-auto pt-[20px]">
      <label>
        <input id="input" type="checkbox" v-model="isDark">
        <span class="check"></span>
      </label>

      <div class="flex">
        <div class=" w-[30%] m-5">
          <div class="shadow-md w-[400px] bg-white dark:bg-slate-900 rounded-xl border border-gray-300 dark:border-white border-solid p-5">
            <div>
              <TitleHandler name="Upcomming Sessions" date="Saturday, June 25, 2022" plus="+" />
            </div>

            <div class="my-4">
              <swiper />
            </div>

            <div>
              <JoinBox imgUrl="image1" title="Baraka (YC S21)" para="Investing, Empowered." date=" 11 : 00 AM to 11: 30 AM " />
            </div>

            <div>
              <CommonBox imgUrl="image2" title="Memorisely" para="E-Learning" date=" 11 : 00 AM to 11: 30 AM " />
            </div>

            <div>
              <CommonBox imgUrl="image3" title="Memorisely" para="The Evolution of A Revolution" date=" 11 : 00 AM to 11: 30 AM " />
            </div>

            <div>
              <CommonBox imgUrl="image4" title="Memorisely" para="The Evolution of A Revolution" date=" 11 : 00 AM to 11: 30 AM " />
            </div>

          </div>
        </div>
        <div class=" w-[60%] my-5">
          <div class="shadow-md w-[400px] bg-white dark:bg-slate-900 rounded-xl border border-gray-300 dark:border-white border-solid p-5">
            <div>
              <TitleHandler name="Upcomming Sessions" date="Saturday, June 25, 2022" plus="+" />
            </div>

            <div class="my-4">
              <swiper />
            </div>

            <div>
              <div class="shadow my-4 p-4 bg-white dark:bg-[#282c41] rounded-lg">
                <div class="flex items-center justify-center">
                    <div class=" text-center">
                        <img src="../assets/Music.png" class=" w-auto mr-3" alt="Img">
                        <h2  class=" text-[#282C41] dark:text-white text-[13px] font-medium ">You have <span class=" text-[#282C41] dark:text-white text-[15px] font-bold ">no upcoming <br> sessions</span>  - start sharing a <br> conversation with a mentor.</h2>
                    </div>
                  </div>
              </div>
            </div>


          </div>
        </div>
        <div class=" w-[30%] my-5">
          <div class="shadow-md w-[400px] bg-white dark:bg-slate-900 rounded-xl border border-gray-300 dark:border-white border-solid p-5">
            <div>
              <TitleHandler name="Upcomming Sessions" date="Saturday, June 25, 2022" plus="+" />
            </div>

            <div class="my-4">
              <swiper />
            </div>

            <div>
              <JoinBox imgUrl="image1" title="Baraka (YC S21)" para="Investing, Empowered." date=" 11 : 00 AM to 11: 30 AM " />
            </div>

            <div>
              <CommonBox imgUrl="image2" title="Memorisely" para="E-Learning" date=" 11 : 00 AM to 11: 30 AM " />
            </div>

            <div>
              <CommonBox imgUrl="image3" title="Memorisely" para="The Evolution of A Revolution" date=" 11 : 00 AM to 11: 30 AM " />
            </div>

            <div>
              <CommonBox imgUrl="image4" title="Memorisely" para="The Evolution of A Revolution" date=" 11 : 00 AM to 11: 30 AM " />
            </div>

          </div>
        </div>
      </div>
    </div>



  </div>
</template>

<script setup>
// @ is an alias to /src
import JoinBox from '@/components/JoinBox.vue';
import CommonBox from '@/components/CommonBox.vue';
import TitleHandler from '@/components/TitleHandler.vue';
import swiper from '@/components/swiper.vue'
import { provide } from 'vue';
import { useDark, useToggle } from '@vueuse/core'
import { ref } from 'vue';
const imgData = ref("../assets/image1.png");
const isDark = useDark()
const toggleDark = useToggle(isDark)

// const products = ref([
//   {
//     img: "image1.png",
//     title: "One shoulder bow top",
    
//   }
// ])

</script>


<style scoped>
/* input style */
input[type="checkbox"] {
  -webkit-appearance: none;
  appearance: none;
  visibility: hidden;
  display: none;
}

.check {
  position: relative;
  display: block;
  width: 80px;
  height: 36px;
  background-color: #092c3e;
  cursor: pointer;
  border-radius: 20px;
  overflow: hidden;
  transition: ease-in 0.5s;
}

input:checked[type="checkbox"]~.check {
  background-color: #fff;
  /*   box-shadow: 0 0 0 1200px #092c3e; */
}

.check:before {
  content: '';
  position: absolute;
  top: 3px;
  left: 4px;
  background-color: #fff;
  width: 30px;
  height: 30px;
  border-radius: 50%;
  transition: all 0.5s;
}

input:checked[type="checkbox"]~.check:before {
  transform: translateX(-50px);
}

.check:after {
  content: '';
  position: absolute;
  top: 3px;
  right: 4px;
  background-color: #092c3e;
  width: 30px;
  height: 30px;
  border-radius: 50%;
  transform: translateX(50px);
  transition: all 0.5s;

}

input:checked[type="checkbox"]~.check:after {
  transform: translateX(0px);
}
</style>
