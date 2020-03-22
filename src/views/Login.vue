<template>
    <div class="w-full">
        <div class="w-full max-w-xs m-auto">
           <form @submit.prevent="submit" class="bg-white shadow-md rounded px-8 pt-6 pb-8 mb-4 align-middle">
                <div class="mb-4">
                    <label class="block text-gray-700 text-sm font-bold mb-2" for="email">
                        Email
                    </label>
                    <input class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline" id="email" type="text" placeholder="fulan@tester.id" v-model="form.email">
                </div>
                <div class="mb-4">
                    <label class="block text-gray-700 text-sm font-bold mb-2" for="password">
                        Password
                    </label>
                    <input class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline" id="password" type="password" placeholder="12345" v-model="form.password">
                </div>
                <button class="bg-blue-500 w-full hover:bg-blue-700 text-white font-bold py-2 px-4 rounded focus:outline-none focus:shadow-outline" type="submit">
                    Masuk
                </button>
           </form>
        </div>
    </div>
</template>

<script>
import axios from 'axios'
export default {
    data () {
        return {
            form: {
                email: null,
                password: null
            }
        }
    },
    methods: {
        submit () {
            let response = axios.post('https://albani-jwt.herokuapp.com/api/auth/signin', this.form);
            console.log(response.data)
        }
    }
}
</script>