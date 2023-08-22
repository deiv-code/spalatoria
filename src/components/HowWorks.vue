<template>
    <div class="md:flex align-middle img pb-10">
        <div class="lg:w-6/12"></div>
        <div class="lg:w-6/12 px-3 md:pl-10 md:py-10 text">
            <div class="pl-2">
                <h3 class="text-[40px] font-bold md:my-10">{{ language === 'en' ? 'How It Works' : "Cum funcționează"}}</h3>
                <span>{{language === 'en' ? 'Using our self-service laundromat is a breeze. Follow these simple steps to have your laundry cleaned and refreshed in no time:' : 
                'Utilizarea spălătoriei noastre self-service este extrem de ușoară. Urmați acești pași simpli pentru a vă curăța și proaspăta rufele într-un timp scurt:'}}</span>
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
    import {store} from '../store'
    export default {
        computed: {
            allSteps() {
                return {
                    en: [
                        {
                            url: '../../public/cashier.svg',
                            title: 'Bring in your laundry and choose a washing machine. Insert your payment using our convenient payment system.'
                        },
                        {
                            url: '../../public/step-washing.svg',
                            title: 'Load your clothes into the machine and select the number of the machine with your preferred wash settings.'
                        },
                        {
                            url: '../../clean-clothes.svg',
                            title: 'Start the washing cycle and let our machines do the work. Once done, transfer your clothes to a dryer and choose the drying settings.'
                        },
                        {
                            url: '../../coffee.svg',
                            title: "After the drying cycle, your laundry is ready. Collect your clean and fresh clothes, and you're all set to tackle your day with confidence."
                        },
                    ],
                    ro: [
                        {
                        url: '../../public/cashier.svg',
                        title: 'Aduceți-vă rufele și alegeți o mașină de spălat. Introduceți plata folosind sistemul nostru comod de plată.',
                        },
                        {
                        url: '../../public/step-washing.svg',
                        title: 'Încărcați hainele în mașină și selectați numărul mașinii cu setările preferate de spălare.',
                        },
                        {
                        url: '../../clean-clothes.svg',
                        title: 'Porniți ciclul de spălare și lăsați mașinile noastre să lucreze. După finalizare, transferați hainele într-un uscător și alegeți setările de uscare.',
                        },
                        {
                        url: '../../coffee.svg',
                        title: 'După ciclul de uscare, rufele dvs. sunt gata. Ridicați hainele curate și proaspete și sunteți pregătit să vă abordați ziua cu încredere.',
                        },
                    ]
                }
            },
            steps() {
                return this.allSteps[store.language] || [];
            },
            language() {
                return store.language
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