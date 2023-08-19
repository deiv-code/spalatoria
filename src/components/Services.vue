<template>
    <div class="services-container pb-20">
        <h1 class="text-center py-12 text-[40px] tracking-wider">FEATURED SERVICES</h1>
        <div class="grid grid-cols-1 md:grid-cols-3 gap-4 md:ml-32 md:mr-32 ml-10 mr-10">
            <div class="border text-center p-10"  v-for="(service, index) in services" :key="index">
                <img class="w-20 m-auto py-8" :src="service.url" alt="">
                <h4 class="font-bold text-xl">{{ service.title }}</h4>
                <span>{{ service.subtitle }}</span>
            </div>

        </div>
    </div>
</template>

<script>

    export default {
        data() {
            return {
                services: [
                {
                    url: "../../washing.svg",
                    title: 'Self-Service Washing & Drying',
                    subtitle: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiuscidre et dolore magna'
                },
                {
                    url: "../../clothes.svg",
                    title: 'Self-Service Washing & Drying',
                    subtitle: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiuscidre et dolore magna'
                },
                {
                    url: "../../detergent.svg",
                    title: 'Self-Service Washing & Drying',
                    subtitle: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiuscidre et dolore magna'
                },
                {
                    url: "../../clock.svg",
                    title: 'Self-Service Washing & Drying',
                    subtitle: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiuscidre et dolore magna'
                },
                {
                    url: "../../wifi.svg",
                    title: 'Self-Service Washing & Drying',
                    subtitle: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiuscidre et dolore magna'
                },
                {
                    url: "../../bucket.svg",
                    title: 'Self-Service Washing & Drying',
                    subtitle: 'Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiuscidre et dolore magna'
                },
            ]
            }
           
        }
    }

</script>

<style scoped lang="scss">
    .services-container {
        background-color: #F7F7F7;
    }
</style>