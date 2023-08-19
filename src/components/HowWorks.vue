<template>
    <div class="md:flex align-middle img pb-10">
        <div class="lg:w-6/12"></div>
        <div class="lg:w-6/12 md:pl-10 md:py-10 text">
            <div class="pl-10">
                <h3 class="text-[40px] font-bold md:my-10">How It Works</h3>
                <span>Lorem ipsum dolor sit amet consectetur adipisicing elit. Porro dolorem, tenetur dolores facere cupiditate ullam? Iure, voluptatibus quam nemo, aperiam itaque, inventore suscipit cum eos modi cupiditate delectus corrupti? Excepturi.</span>
            </div>
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-2">
                <div class="mt-20" v-for="(step, index) in steps" :key="index">
                    <div class="bg-slate-100 border rounded-full p-5 relative h-32 w-32 m-auto">
                        <img :src="step.url" class="m-auto w-16 h-16" alt="">
                        <div class="w-12 h-12 rounded-full bg-cyan-400 text-white absolute top-[75%] left-[50%] translate-x-[-50%] flex items-center justify-center font-bold">{{ index+1 }}</div>
                    </div>
                    <h3 class="text-center mt-5 font-bold ">{{ step.title }}</h3>
                </div>
                
            </div>
        </div>
    </div>
</template>

<script>

    export default {
        data() {
            return {
                steps: [
                    {
                        url: '../../public/cashier.svg',
                        title: 'At the cashier insert the money'
                    },
                    {
                        url: '../../public/step-washing.svg',
                        title: 'Select the number of the washing/drying machine'
                    },
                    {
                        url: '../../clean-clothes.svg',
                        title: 'Your clothes are clean and dry'
                    },
                    {
                        url: '../../coffee.svg',
                        title: 'Relax and enjoy your clean laundry'
                    },
                ]
            }
        }
    }

</script>

<style scoped lang="scss">
    .img {
        background-image: url('/clothes-table.jpg');
        background-repeat: no-repeat;
        background-size: cover;
        background-position: center;
    }

</style>