<template>
  <div>
    <div class="min-h-screen bg-gray-100">
      <nav class="bg-white border-b border-gray-100"  >
        <!-- Primary Navigation Menu -->
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
          <div class="flex justify-between h-20">
            <div class="flex">
              <!-- Logo -->
              <div class="flex-shrink-0 flex items-left">
                <Link :href="route('gusers.lending_page')">
                  <BreezeApplicationLogo class="block h-20 w-auto" />
                </Link>
              </div>
               <div class="flex items-center ml-6">
                <BreezeDropdownLink :href="route('gusers.lending_page')">
                  Home
                </BreezeDropdownLink>
              </div>
               <div class="flex items-center ml-6">
                <BreezeDropdownLink :href="route('gusers.login')">
                  Login
                </BreezeDropdownLink>
              </div>
               <div class="flex items-center ml-6">
                <BreezeDropdownLink :href="route('gusers.register')">
                  Register
                </BreezeDropdownLink>
              </div>
               <div class="flex items-center ml-6">
                <BreezeDropdownLink :href="route('guser.aboutus')">
                  About Us
                </BreezeDropdownLink>
              </div>
               <div class="flex items-center ml-6">
                <BreezeDropdownLink :href="route('guser.contactus')">
                  Contact Us
                </BreezeDropdownLink>
              </div>
            </div>


          </div>
        </div>

      </nav>

      <!-- Page Content -->
      <main class="min-w-full">
        <h1 class="text-center py-6 text-6xl font-bold">The Party Time is a website for the customer  for their event business and the customers will have a valuable and simple website to book and get services they desire and love.</h1>
      </main>
    </div>
  </div>
  <Footer />
</template>

<script>
import BreezeApplicationLogo from "@/Components/ApplicationLogo.vue";
import BreezeDropdown from "@/Components/Dropdown.vue";
import BreezeDropdownLink from "@/Components/DropdownLink.vue";
import BreezeNavLink from "@/Components/NavLink.vue";
import BreezeResponsiveNavLink from "@/Components/ResponsiveNavLink.vue";
import { Link } from "@inertiajs/inertia-vue3";
import Footer from '@/Components/FooterUser.vue'

export default {
  components: {
    BreezeApplicationLogo,
    BreezeDropdown,
    BreezeDropdownLink,
    BreezeNavLink,
    BreezeResponsiveNavLink,
    Link,
    Footer
  },
  props: {
    isLoggedIn: {
      type: Boolean,
      default: false,
    },
  },

};
</script>
