<template>
    <div
        class="bg-gray-600 min-h-screen flex justify-center items-center min-w-full p-12 text-white"
    >
        <div class="bg-white rounded-lg shadow-lg p-12 w-1/3">
            <h1 class="text-black w-full text-center">Register</h1>
            <form @submit.prevent="submitForm">
                <input
                    class="w-full border-2 shadow mt-2 p-2 text-black"
                    v-model="formData.full_name"
                    placeholder="Full Name"
                />
                <input
                    class="w-full border-2 shadow mt-2 p-2 text-black"
                    v-model="formData.email"
                    placeholder="Email"
                />
                <input
                    class="w-full border-2 shadow mt-2 p-2 text-black"
                    v-model="formData.phone"
                    placeholder="Phone"
                />
                <input
                    class="w-full border-2 shadow mt-2 p-2 text-black"
                    v-model="formData.shipping_address"
                    placeholder="Billing Address"
                />
                <input
                    class="w-full border-2 shadow mt-2 p-2 text-black"
                    v-model="formData.billing_address"
                    type="address"
                    placeholder="Shipping Address"
                />
                <!-- <div class="relative">
                    <input
                        class="w-full border-2 shadow mt-2 p-2 text-black"
                        v-model="formData.password"
                        type="password"
                        placeholder="Password"
                    />
                </div> -->
                <div class="relative w-full">
                    <div
                        class="absolute inset-y-0 right-0 flex items-center px-2"
                    >
                        <input
                            class="hidden js-password-toggle"
                            id="toggle"
                            type="checkbox"
                        />
                        <label
                            class="mt-2 rounded px-2 py-1 text-sm text-gray-600 font-mono cursor-pointer js-password-label"
                            for="toggle"
                            @click="togglePassword = !togglePassword"
                        >
                            <svg
                                version="1.1"
                                id="Capa_1"
                                xmlns="http://www.w3.org/2000/svg"
                                xmlns:xlink="http://www.w3.org/1999/xlink"
                                x="0px"
                                y="0px"
                                width="20.04px"
                                height="20.04px"
                                viewBox="0 0 442.04 442.04"
                                style="enable-background: new 0 0 442.04 442.04"
                                xml:space="preserve"
                            >
                                <g>
                                    <g>
                                        <path
                                            d="M221.02,341.304c-49.708,0-103.206-19.44-154.71-56.22C27.808,257.59,4.044,230.351,3.051,229.203
			c-4.068-4.697-4.068-11.669,0-16.367c0.993-1.146,24.756-28.387,63.259-55.881c51.505-36.777,105.003-56.219,154.71-56.219
			c49.708,0,103.207,19.441,154.71,56.219c38.502,27.494,62.266,54.734,63.259,55.881c4.068,4.697,4.068,11.669,0,16.367
			c-0.993,1.146-24.756,28.387-63.259,55.881C324.227,321.863,270.729,341.304,221.02,341.304z M29.638,221.021
			c9.61,9.799,27.747,27.03,51.694,44.071c32.83,23.361,83.714,51.212,139.688,51.212s106.859-27.851,139.688-51.212
			c23.944-17.038,42.082-34.271,51.694-44.071c-9.609-9.799-27.747-27.03-51.694-44.071
			c-32.829-23.362-83.714-51.212-139.688-51.212s-106.858,27.85-139.688,51.212C57.388,193.988,39.25,211.219,29.638,221.021z"
                                        />
                                    </g>
                                    <g>
                                        <path
                                            d="M221.02,298.521c-42.734,0-77.5-34.767-77.5-77.5c0-42.733,34.766-77.5,77.5-77.5c18.794,0,36.924,6.814,51.048,19.188
			c5.193,4.549,5.715,12.446,1.166,17.639c-4.549,5.193-12.447,5.714-17.639,1.166c-9.564-8.379-21.844-12.993-34.576-12.993
			c-28.949,0-52.5,23.552-52.5,52.5s23.551,52.5,52.5,52.5c28.95,0,52.5-23.552,52.5-52.5c0-6.903,5.597-12.5,12.5-12.5
			s12.5,5.597,12.5,12.5C298.521,263.754,263.754,298.521,221.02,298.521z"
                                        />
                                    </g>
                                    <g>
                                        <path
                                            d="M221.02,246.021c-13.785,0-25-11.215-25-25s11.215-25,25-25c13.786,0,25,11.215,25,25S234.806,246.021,221.02,246.021z"
                                        />
                                    </g>
                                </g>
                                <g></g>
                                <g></g>
                                <g></g>
                                <g></g>
                                <g></g>
                                <g></g>
                                <g></g>
                                <g></g>
                                <g></g>
                                <g></g>
                                <g></g>
                                <g></g>
                                <g></g>
                                <g></g>
                                <g></g>
                            </svg>
                        </label>
                    </div>
                    <input
                        class="w-full border-2 shadow mt-2 p-2 text-black border-gray-200"
                        id="password"
                        :type="togglePassword ? 'text' : 'password'"
                        placeholder="Password"
                        autocomplete="off"
                    />
                </div>
                <div class="w-full text-center">
                    <button
                        type="submit"
                        class="bg-green-500 rounded-lg shadow-lg px-6 py-2 mt-4"
                    >
                        Register
                    </button>
                </div>
            </form>
            <h1 class="w-full text-center text-black text-sm mt-6">
                Already Have Account?
                <Link :href="route('gusers.login')" class="underline text-black"
                    >Login Now!</Link
                >
            </h1>
        </div>
    </div>
</template>

<script>
import { Link } from "@inertiajs/inertia-vue3";

export default {
    components: {
        Link,
    },
    data() {
        return {
            formData: {
                full_name: "",
                email: "",
                phone: "",
                shipping_address: "",
                billing_address: "",
                password: "",
            },
            togglePassword: false,
        };
    },

    methods: {
        submitForm() {
            axios.post("/register", this.formData).then((res) => {
                window.location = "/";
            });
        },
    },
};
</script>

<style lang="scss" scoped></style>
