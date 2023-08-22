<template>
    <div class="services-container pb-20">
        <h1 class="text-center py-12 text-[40px] tracking-wider">{{language === 'en' ? 'FEATURED SERVICES' : 'SERVICIILE NOASTRE'}}</h1>
        <div class="grid grid-cols-1 md:grid-cols-3 gap-4 md:ml-32 md:mr-32 ml-10 mr-10">
            <div class="border text-center p-8"  v-for="(service, index) in services" :key="index">
                <img class="w-20 m-auto pb-6" :src="service.url" alt="">
                <h4 class="font-bold text-xl pb-5">{{ service.title }}</h4>
                <span>{{ service.subtitle }}</span>
            </div>

        </div>
    </div>
</template>

<script>
    import {store} from '../store'
    export default {

        computed: {
            services() {
                return this.allServices[store.language] || [];
            },
            allServices() {
                  return {
                    en: [
                        {
                            url: "../../washing.svg",
                            title: 'Self-Service Washing & Drying',
                            subtitle: 'Experience the ultimate convenience with our Express Wash & Dry service. Drop off your laundry, and our high-capacity machines will have your clothes cleaned, dried, and ready for pick-up in no time.'
                        },
                        {
                            url: "../../clothes.svg",
                            title: 'Gentle Care Delicates',
                            subtitle: 'Trust us with your most delicate garments. Our Gentle Care Delicates service uses specialized washing techniques and mild detergents to ensure your fragile fabrics, lace, and fine garments receive the tender loving care they deserve.'
                        },
                        {
                            url: "../../detergent.svg",
                            title: 'Premium In-House Detergent',
                            subtitle: 'Our laundromat provides high-quality detergents that are specially formulated to work seamlessly with our machines, guaranteeing optimal cleaning and fabric care. With our in-house detergent service, you can trust that your clothes will emerge clean, fresh, and beautifully maintained, without the hassle of bringing your own supplies.'
                        },
                        {
                            url: "../../clock.svg",
                            title: '1-Hour Laundry Boost',
                            subtitle: 'Get your laundry done lightning-fast with our 1-Hour Laundry Boost. Drop off your clothes, and in just 60 minutes, our advanced machines will wash and dry them to perfection. Enjoy clean, fresh laundry without the wait!'
                        },
                        {
                            url: "../../wifi.svg",
                            title: 'Stain Removal',
                            subtitle: 'Say goodbye to stubborn stains! Our Stain Removal Experts service employs advanced stain-fighting techniques to tackle even the toughest marks, leaving your clothes spotless and looking as good as new.'
                        },
                        {
                            url: "../../bucket.svg",
                            title: 'Large Loads, Quick Loads',
                            subtitle: "Don't stress about big loads of laundry. Our Large Loads, Quick Loads service lets you tackle bulky items like comforters, bed linens, and family-sized laundry loads efficiently and affordably, all while maintaining the quality your clothes deserve."
                        },
                    ],
                    ro: [
                    {
                        url: "../../washing.svg",
                        title: 'Spălare și Uscare Self-Service',
                        subtitle: 'Experimentați ultima comoditate cu serviciul nostru Express Spălare și Uscare. Lăsați-vă rufele, iar mașinile noastre de mare capacitate le vor spăla, usca și pregăti pentru ridicare într-un timp scurt.'
                    },
                    {
                        url: "../../clothes.svg",
                        title: 'Delicatețe cu Îngrijire Blândă',
                        subtitle: 'Aveți încredere în noi cu cele mai delicate articole vestimentare. Serviciul nostru Delicatețe cu Îngrijire Blândă utilizează tehnici de spălare specializate și detergenți blânzi pentru a vă asigura că materialele fragile, dantela și articolele fine primesc îngrijirea delicată pe care o merită.'
                    },
                    {
                        url: "../../detergent.svg",
                        title: 'Detergent Premium în Propriul Atelier',
                        subtitle: 'Laundry noastră oferă detergenți de înaltă calitate, special formulați pentru a funcționa perfect cu mașinile noastre, garantând o curățare optimă și îngrijire a țesăturilor. Cu serviciul nostru de detergent intern, puteți avea încredere că rufele dumneavoastră vor ieși curate, proaspete și frumos întreținute, fără neplăcerile aduse de aducerea propriilor provizii.'
                    },
                    {
                        url: "../../clock.svg",
                        title: 'Accelerare Spălare în 1 Ora',
                        subtitle: 'Realizați-vă spălătoria într-un timp record cu serviciul nostru de Accelerare Spălare în 1 Ora. Lăsați-vă hainele, iar în doar 60 de minute, mașinile noastre avansate le vor spăla și usca perfect. Bucurați-vă de haine curate și proaspete fără a mai aștepta!'
                    },
                    {
                        url: "../../wifi.svg",
                        title: 'Îndepărtare Petice',
                        subtitle: 'Spuneți adio petelor dificile! Serviciul nostru de Îndepărtare Petice utilizează tehnici avansate de luptă împotriva petelor pentru a elimina chiar și cele mai persistente urme, lăsându-vă hainele impecabile și arătând ca noi.'
                    },
                    {
                        url: "../../bucket.svg",
                        title: 'Încărcături Mari, Spălări Rapide',
                        subtitle: 'Nu vă faceți griji în privința încărcăturilor mari de rufe. Serviciul nostru Încărcături Mari, Spălări Rapide vă permite să vă ocupați eficient și convenabil de articolele voluminoase precum cuverturile, lenjeriile de pat și încărcăturile mari de familie, păstrând în același timp calitatea hainelor dumneavoastră.'
                    }

                    ]
                }
                },
                language() {
                return store.language
            }
        },
  
    }

</script>

<style scoped lang="scss">
    .services-container {
        background-color: #F7F7F7;
    }
</style>