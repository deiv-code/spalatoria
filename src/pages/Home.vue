<template>
    <main class="pt-36  md:h-[600px] flex justify-center items-center">
        <div class="text-white text-[16px] h-full">
            <h1 class="md:text-[80px] text-[60px] font-bold w-[20rem] leading-[0.9]">Self-service Laundromat in <span class="text-cyan-500">Oradea</span></h1>
        </div>
    </main>
    <Services></Services>
    <HowWorks></HowWorks>
    <Prices></Prices>
    <FAQ></FAQ>
    <Footer></Footer>
</template>

<script>
    import Services from '../components/Services.vue'
    import HowWorks from '../components/HowWorks.vue'
    import Prices from '../components/Prices.vue'
    import FAQ from '../components/FAQ.vue'
    import Footer from '../components/Footer.vue'
    export default {
    components: {
      Services,
      HowWorks,
      Prices,
      FAQ,
      Footer
    }
  }
</script>

<style lang="scss" scoped>
    main {
        height: 600px;
        width: 100%;
        background-image: linear-gradient(90deg, rgba(9,9,121,0.3) 37%, rgba(0,212,255,0.3) 100%), url('https://show.moxcreative.com/cleanox/wp-content/uploads/sites/11/2021/11/laundry-room-with-a-washing-machine-scaled.jpg');
        opacity: 0.6;
        background-position: center;
        background-repeat: no-repeat;
        background-size: cover;
        transition: background 0.3s, border-radius 0.3s, opacity 0.3s;
        z-index: 9999;

       
    }
</style>