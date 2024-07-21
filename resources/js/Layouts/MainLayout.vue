<template>
    <div class="fixed w-full">
        <div class="max-w-[1400px] flex mx-auto">
            <div
                class="lg:w-3/12 w-[60px] h-[100vh] max-w-[350px] lg:px-4 lg:mx-auto"
            >
                <div class="p-2 px-3 mb-4">
                    <Heart fillColor="pink" :size="37" />
                </div>
                <MenuItem iconString="Home" />
                <MenuItem iconString="Explore" />
                <MenuItem iconString="Notifications" />
                <MenuItem iconString="Messages" />
                <MenuItem iconString="Profile" />

                <button
                    class="lg:w-full mt-8 text-white font-extrabold text-[22px] bg-pink-800 ml-1.5 lg:ml-0 p-3 px-3 rounded-full cursor-pointer hover:bg-pink-600"
                >
                    <span class="lg:block hidden">Meetz</span>
                    <span class="block lg:hidden"><Feather /></span>
                </button>
            </div>
            <div class="lg:w-7/12 w-11/12 border-x border-gray-800 relative">
                <div
                    class="bg-[#131313] bg-opacity-50 backdrop-blur-md z-10 absolute w-full"
                >
                    <div class="border-gray-800 border-b w-full">
                        <div
                            class="w-full text-white text-[22px] font-extrabold p-4"
                        >
                            Home
                        </div>
                        <div class="flex">
                            <div
                                class="flex items-center justify-center text-white w-full h-[60px] text-[17px] font-extrabold p-4 hover:bg-pink-500 hover:bg-opacity-30 cursor-pointer transition duration-200 ease-in-out"
                            >
                                <div
                                    class="inline-block text-center border-b-4 border-b-pink-500 h-[60px]"
                                >
                                    <div class="my-auto mt-4">For you</div>
                                </div>
                            </div>
                            <div
                                class="text-gray-500 w-full h-[60px] text-[17px] font-extrabold p-4 hover:bg-pink-500 hover:bg-opacity-30 cursor-pointer transition duration-200 ease-in-out"
                            >
                                <div class="text-center">Following</div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
            <div class="absolute top-0 z-0 h-full overflow-auto scrollbar-hide">
                <div class="mt-[126px]"></div>
                <slot />
                <div class="pb-4"></div>
            </div>
            <div
                class="lg:block hidden lg:w-4/12 h-screen border-l border-gray-800 pl-4"
            >
                <div
                    class="w-full p-1 mt-2 px-4 lg:flex items-center rounded-full hidden bg-pink-950"
                >
                    <Magnify fillColor="#5E5C5C" size="25" />
                    <input
                        class="appearance-none w-full border-0 py-2 bg-pink-950 text-gray-100 placeholder-gray-500 leading-tight focus:ring-0"
                        type="text"
                        placeholder="Search Meetz"
                    />
                </div>
                <div
                    class="w-full mt-4 rounded-lg lg:block hidden bg-[#212327]"
                >
                    <div
                        class="w-full p-4 text-white font-extrabold mb-6 text-[20px]"
                    >
                        What's happening
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script setup>
import { ref } from "vue";
import { router } from "@inertiajs/vue3";
import Heart from "vue-material-design-icons/Heart.vue";
import Magnify from "vue-material-design-icons/Magnify.vue";
import DotsHorizontal from "vue-material-design-icons/DotsHorizontal.vue";
import Feather from "vue-material-design-icons/Feather.vue";
import Close from "vue-material-design-icons/Close.vue";
import ChevronDown from "vue-material-design-icons/ChevronDown.vue";
import Earth from "vue-material-design-icons/Earth.vue";
import ImageOutline from "vue-material-design-icons/ImageOutline.vue";
import FileGifBox from "vue-material-design-icons/FileGifBox.vue";
import Emoticon from "vue-material-design-icons/Emoticon.vue";
import ArrowLeft from "vue-material-design-icons/ArrowLeft.vue";
import MenuItem from "@/Components/MenuItem.vue";
</script>

<style>
body {
    background-color: #131313;
}
</style>
