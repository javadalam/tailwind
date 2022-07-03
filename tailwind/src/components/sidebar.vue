<template>
  <div class="sidebar">
    <!-- sidebar -->
    <div
      class="bg-cyan-600 text-cyan-100 w-64 space-y-6 px-2 py-4 absolute inset-y-0 left-0 md:relative md:-translate-x-0 transform -translate-x-full transition duration-200 ease-in-out"
      :class="{ 'relative -translate-x-0': showSidebar }"
    >
      <a href="" class="main">
        <svg
          xmlns="http://www.w3.org/2000/svg"
          class="h-10 w-10"
          fill="none"
          viewBox="0 0 24 24"
          stroke="currentColor"
          stroke-width="2"
        >
          <path
            stroke-linecap="round"
            stroke-linejoin="round"
            d="M14 10l-2 1m0 0l-2-1m2 1v2.5M20 7l-2 1m2-1l-2-1m2 1v2.5M14 4l-2-1-2 1M4 7l2-1M4 7l2 1M4 7v2.5M12 21l-2-1m2 1l2-1m-2 1v-2.5M6 18l-2-1v-2.5M18 18l2-1v-2.5"
          />
        </svg>
        <span class="text-2xl font-extrabold text-white hover:text-green-500"
          >Home</span
        >
      </a>

      <nav>
        <a href="/" class="navbar group">
          <svg
            xmlns="http://www.w3.org/2000/svg"
            class="h-6 w-6"
            fill="none"
            viewBox="0 0 24 24"
            stroke="currentColor"
            stroke-width="2"
          >
            <path
              stroke-linecap="round"
              stroke-linejoin="round"
              d="M3 12l2-2m0 0l7-7 7 7M5 10v10a1 1 0 001 1h3m10-11l2 2m-2-2v10a1 1 0 01-1 1h-3m-6 0a1 1 0 001-1v-4a1 1 0 011-1h2a1 1 0 011 1v4a1 1 0 001 1m-6 0h6"
            />
          </svg>
          <span class="navbar--item">Dashbord</span></a
        >

        <a href="/" class="navbar group">
          <svg
            xmlns="http://www.w3.org/2000/svg"
            class="h-6 w-6"
            fill="none"
            viewBox="0 0 24 24"
            stroke="currentColor"
            stroke-width="2"
          >
            <path
              stroke-linecap="round"
              stroke-linejoin="round"
              d="M12 4.354a4 4 0 110 5.292M15 21H3v-1a6 6 0 0112 0v1zm0 0h6v-1a6 6 0 00-9-5.197M13 7a4 4 0 11-8 0 4 4 0 018 0z"
            /></svg
          ><span class="navbar--item">Team</span></a
        >
        <a href="/" class="navbar group">
          <svg
            xmlns="http://www.w3.org/2000/svg"
            class="h-6 w-6"
            fill="none"
            viewBox="0 0 24 24"
            stroke="currentColor"
            stroke-width="2"
          >
            <path
              stroke-linecap="round"
              stroke-linejoin="round"
              d="M9 12h6m-6 4h6m2 5H7a2 2 0 01-2-2V5a2 2 0 012-2h5.586a1 1 0 01.707.293l5.414 5.414a1 1 0 01.293.707V19a2 2 0 01-2 2z"
            /></svg
          ><span class="navbar--item">Project</span>
        </a>

        <a href="/" class="navbar group transition duration-300">
          <svg
            xmlns="http://www.w3.org/2000/svg"
            class="h-6 w-6"
            fill="none"
            viewBox="0 0 24 24"
            stroke="currentColor"
            stroke-width="2"
          >
            <path
              stroke-linecap="round"
              stroke-linejoin="round"
              d="M8 7V3m8 4V3m-9 8h10M5 21h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v12a2 2 0 002 2z"
            /></svg
          ><span class="navbar--item">Calender</span></a
        >
        <a href="/"></a>
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