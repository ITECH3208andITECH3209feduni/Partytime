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
        <h1 class="text-center py-4 text-6xl font-bold">Contact Information</h1>
        <h1 class="text-center py-4 text-3xl font-bold">Give us a call: 000000000</h1>
        <h1 class="text-center py-4 text-3xl font-bold">Send us an email: sample-email@gmail.com</h1>
       
        <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3271.3396017276827!2d138.60038551534217!3d-34.923018980378075!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x6ab0ced418957257%3A0x34877b9b34a650ac!2sApple%20Rundle%20Place!5e0!3m2!1sen!2sau!4v1652365617569!5m2!1sen!2sau" width="1900" height="600" style="border:0;" allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
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
