<template>
    <div class="pb-10 text-center">
        <h1 class="py-10 text-3xl font-light tracking-wide">{{language === 'en' ? 'AFFORDABLE PRICES' : "PRETURILE NOASTRE"}}</h1>
        <div class="grid grid-cols-1 md:grid-cols-3 gap-2 lg:ml-60 lg:mr-60 md:ml-40 md:mr-40 ml-10 mr-10">
            <div class="border text-center rounded">
                <div class="w-full h-1 bg-cyan-400 rounded"></div>
                <h3 class="py-3 px-10 text-2xl font-bold">{{language === 'en' ? 'Washer' : "Mașină de spălat"}}</h3>
                <h5 class="py-2 text-lg">30min</h5>
                <hr>
                <ul>
                    <li class="my-2">10kg - 25 Ron</li>
                    <li class="my-2">14kg - 30 Ron</li>
                </ul>
            </div>
            <div class="border text-center rounded">
                <div class="w-full bg-cyan-400 text-white">
                        <h3 class="py-3 px-10 text-2xl font-bold">{{language === 'en' ? 'Washer & Dryer' : "Mașină de spălat și uscător"}}</h3>
                <h5 class="py-2 text-lg">1hr</h5>
                </div>

                <ul>
                    <li class="my-2">{{language === 'en' ?'10kg Washing Machine + 20 min dryer - 35 Ron' : 
"Mașină de spălat 10 kg + Uscător 20 min - 35 Ron"}}</li>
                    <li class="my-2">{{language === 'en' ?'10kg Washing Machine + 20 min dryer - 35 Ron' : 
"Mașină de spălat 14 kg + Uscător 20 min - 40 Ron"}}</li>
                </ul>
            </div>
            <div class="border text-center rounded">
                <div class="w-full h-1 bg-cyan-400 rounded"></div>
                <h3 class="py-3 px-10 text-2xl font-bold">{{language === 'en' ? 'Dryer' : 'Uscator'}}</h3>
                <h5 class="py-2 text-lg">{{language === 'en' ? 'Select your preferred time' : "Selectați timpul preferat"}}</h5>
                <hr>
                <ul>
                    <li class="my-2">10 min - 10 Ron</li>
                    <li class="my-2">20 min - 20 Ron</li>
                </ul>
            </div>
        </div>
        
    </div>
</template>

<script>
    import {store} from '../store'

    export default {
        computed: {
            language() {
                return store.language
            }
        }
    }
</script>