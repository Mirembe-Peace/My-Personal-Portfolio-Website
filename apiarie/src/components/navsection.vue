<template>
    <header class= "flex justify-between items-center p-6 bg-opacity-50 relative z-20"> 
        <div class="text-white text-3xl font-bold">apiarie</div>
        <!--Mobile Toggle Button-->
        <button type="button" class="block text- focus:outline-none">
            <span class="text-5xl">
                <img src="./src/assets/close.png" alt="close" width="50" height="50">
            </span>
            <span class="text-5xl">
                <img src="./src/assets/menu.png" alt="menu" width="50" height="50">
            </span>
        </button>

        <!--Navigation Links-->
        <nav>
            <ul class="flex flex-col items-center space-y-5 md:flex-row md:space-x-5 md:space-y-0">
                    <li v-for="item in menu" :key="item.name">
                            <a :href="item.href" class="block text-white transition hover:text-primary ease-linear text-2l md:text-lg">
                                {{  item.name }}
                            </a>
                    </li>
            </ul>
        </nav>
    </header>
</template>

<script setup>
import { ref } from 'vue';
const menu = ref(
    [
        {name: 'Home', href: '#home'},
        {name: 'About', href: '#about'},
        {name: 'Projects', href: '#projects'},
        {name: 'Contact', href: '#contact'},
        {name: 'Blog', href: '#blog'},
    ]
)
</script>