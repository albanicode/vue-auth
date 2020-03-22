<template>
    <div>
        <ul class="flex bg-gray-300 py-3">
            <li class="mr-3 ml-3">
                <router-link :to="{name: 'Home'}" class="text-blue-500 no-underline block hover:text-blue-800">Home</router-link>
            </li>
            <li class="mr-3 ml-3">
                <router-link :to="{name: 'Dashboard'}" class="text-blue-500 no-underline block hover:text-blue-800">Dashboard</router-link>
            </li>
            <li class="mr-3 ml-3">
                <router-link :to="{name: 'About'}" class="text-blue-500 no-underline block hover:text-blue-800">About</router-link>
            </li>
            <li class="mr-3 ml-3">
                <router-link :to="{name: 'Login'}" class="text-blue-500 no-underline block hover:text-blue-800">Login</router-link>
            </li>
        </ul>
    </div>
</template>