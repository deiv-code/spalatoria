<template>

    <nav class="flex justify-between md:justify-around p-4 fixed w-full z-50">
        <div>
            <router-link :to="{name: 'home'}">Logo</router-link>
            <div class="flex flex-col" v-show="showMenu">
                <router-link class="m-2 text-xl" :to="{name: 'home'}">Home</router-link>
                <router-link class="m-2 text-xl" :to="{name: 'home'}">Price</router-link>
                <router-link class="m-2 text-xl" :to="{name: 'home'}">How It Works</router-link>
                <router-link class="m-2 text-xl" :to="{name: 'home'}">Contact Us</router-link>
            </div>
        </div>
        
        <div class="nav-links hidden md:block">
            <router-link class="m-2 text-xl" :to="{name: 'home'}">Home</router-link>
            <router-link class="m-2 text-xl" :to="{name: 'home'}">Price</router-link>
            <router-link class="m-2 text-xl" :to="{name: 'home'}">How It Works</router-link>
            <router-link class="m-2 text-xl" :to="{name: 'home'}">Contact Us</router-link>
        </div>

        <div class="sidemenu md:hidden">
            <button @click="showMenu = !showMenu" class="space-y-1">
                <span class="block w-5 h-1 bg-white rounded"></span>
                <span class="block w-8 h-1 bg-white rounded"></span>
                <span class="block w-8 h-1 bg-white rounded"></span>
            </button>
            
        </div>
       
    </nav>

</template>

<script>
    import {ref} from 'vue'
    
    export default {
        setup() {
            const showMenu = ref(false);

            return {
                showMenu
            }
        }
    }

</script>

<style scoped lang="scss">
    @import '../styles/variables.scss';
    nav {
        background-color: $primary;
        color: white;
        .nav-links > *:hover {
            text-decoration: underline;
        }
    }
</style>