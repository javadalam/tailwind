<template>
  <div class="sidebar">
    <!-- sidebar -->
    <div
      class="bg-cyan-600 text-cyan-100 w-64 space-y-6 px-2 py-4 absolute inset-y-0 left-0 md:relative md:-translate-x-0 transform -translate-x-full transition duration-200 ease-in-out"
      :class="{ 'relative -translate-x-0': showSidebar }"
    >
      <a href="" class="main">
        <i class="bi bi-house"></i>
        <span class="text-2xl font-extrabold text-white">Home</span>
      </a>

      <nav>
        <a href="/" class="navbar group">
          <i class="bi bi-bookmark-dash"></i>
          <span class="navbar--item">Dashbord</span>
        </a>

        <a href="/" class="navbar group">
          <i class="bi bi-people "></i>
          <span class="navbar--item">Team</span>
        </a>
        
        <a href="/" class="navbar group">
         <i class="bi bi-file-earmark-code"></i>
          <span class="navbar--item">Project</span>
        </a>

        <a href="/" class="navbar group transition duration-300">
         <i class="bi bi-calendar"></i>
         <span class="navbar--item">Calender</span>
        </a>

      </nav>
    </div>

    <!-- my content -->

    <div class="flex-1">
      <!-- Header -->
      <div class="bg-white shadow px-2">
        <button
          @click="showSidebar = !showSidebar"
          class="font-extrabold text-cyan-600"
        >
          <svg
            xmlns="http://www.w3.org/2000/svg"
            class="h-8 w-8"
            fill="none"
            viewBox="0 0 24 24"
            stroke="currentColor"
            stroke-width="2"
          >
            <path
              stroke-linecap="round"
              stroke-linejoin="round"
              d="M4 6h16M4 12h8m-8 6h16"
            />
          </svg>
        </button>
      </div>
      <!-- Content -->
      <div class="pt-8 text-gray-600" >
        <div class="login-main">
          <div class="login-main-form">
            <div class="font-extrabold px-20 text-xl">Create Your Account</div>
            <form class="form" action="#" method="POST">
              <div>
                <label for="Email" class="form-lable"> Email Address </label>

                <div class="mt-2">
                  <input id="email" name="email" type="email" autocomplete="email"
                    required class="form-input"/>
                </div>
              </div>
              <div>
                <lable for="password" class="form-lable"> Password </lable>

                <div class="mt-2">
                  <input id="password" name="password" type="password" autocomplete="current-password"
                    required class="form-input"/>
                </div>
              </div>
              
              <div class="flex items-center px-8">
                <input id="terms-and-privacy" name="terms-and-privacy" type="checkbox" class="rounded"/>
                <label for="terms-and-privacy" class="ml-2 block text-sm text-gray-900">I agree to the
                  <a href="#" class="text-indigo-600 hover:text-indigo-500">Terms</a>
                  and
                  <a href="#" class="text-indigo-600 hover:text-indigo-500">Privacy Policy</a>
                </label>
              </div>
            </form>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { ref } from "vue";
export default {
  setup() {
    const showSidebar = ref(false);

    return {
      showSidebar,
    };
  },
};
</script>