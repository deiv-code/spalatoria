<template>

    <nav class="flex justify-between md:justify-around p-4 fixed w-full z-50">
        <div>
            <router-link :to="{name: 'home'}">Logo</router-link>
            <div class="flex flex-col" v-show="showMenu">
                <router-link class="m-2 text-xl" :to="{name: 'home'}">Home</router-link>
                <router-link class="m-2 text-xl" :to="{name: 'home'}">{{currentLanguage === 'en' ? 'Price' : 'Preturi'}}</router-link>
                <router-link class="m-2 text-xl" :to="{name: 'home'}">{{currentLanguage === 'en' ? 'How It Works' : 'Cum funcționează'}}</router-link>
                <router-link class="m-2 text-xl" :to="{name: 'home'}">{{currentLanguage === 'en' ? 'Contact Us' : 'Contact'}}</router-link>
                <a class="m-2 text-xl" @click="changeLanguage()">Change Language</a>
            </div>
        </div>
        
        <div class="nav-links hidden md:block">
            <router-link class="m-2 text-xl" :to="{name: 'home'}">Home</router-link>
            <router-link class="m-2 text-xl" :to="{name: 'home'}">{{currentLanguage === 'en' ? 'Price' : 'Preturi'}}</router-link>
            <router-link class="m-2 text-xl" :to="{name: 'home'}">{{currentLanguage === 'en' ? 'How It Works' : 'Cum funcționează'}}</router-link>
            <router-link class="m-2 text-xl" :to="{name: 'home'}">{{currentLanguage === 'en' ? 'Contact Us' : 'Contact'}}</router-link>
            <a class="m-2 text-xl" @click="changeLanguage()">Change Language</a>
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
    import { ref, computed } from 'vue';
    import {store} from '../store'
    export default {
        setup() {
            const showMenu = ref(false);

            const currentLanguage = computed(() => store.language);

            let changeLanguage = () => {
                store.language = currentLanguage.value === 'ro' ? 'en' : 'ro'
            }

            return {
                showMenu,
                changeLanguage,
                currentLanguage
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