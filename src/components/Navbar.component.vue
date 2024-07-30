<template>
  <nav
    class="bg-custom rounded-lg xs:mt-8 md:mt-6 xs:m-5 sm:m-10 md:m-20 backdrop-blur-3xl"
  >
    <div
      class="max-w-screen-lg flex flex-wrap items-center justify-between mx-auto p-4"
    >
      <RouterLink
        to="/"
        class="flex items-center space-x-3 rtl:space-x-reverse"
      >
        <img src="../assets/img/logo.png" class="h-12" alt="Cowork Logo" />
      </RouterLink>
      <button
        data-collapse-toggle="navbar-solid-bg"
        type="button"
        class="inline-flex items-center p-2 w-10 h-10 justify-center text-sm text-white rounded-lg md:hidden hover:bg-gray-600 focus:outline-none dark:text-gray-400 dark:hover:bg-gray-700"
        aria-controls="navbar-solid-bg"
        aria-expanded="false"
      >
        <span class="sr-only">Abrir menu</span>
        <svg
          class="w-5 h-5"
          aria-hidden="true"
          xmlns="http://www.w3.org/2000/svg"
          fill="none"
          viewBox="0 0 17 14"
        >
          <path
            stroke="currentColor"
            stroke-linecap="round"
            stroke-linejoin="round"
            stroke-width="2"
            d="M1 1h15M1 7h15M1 13h15"
          />
        </svg>
      </button>

      <div class="hidden w-full md:block md:w-auto" id="navbar-solid-bg">
        <ul
          class="text-gray-400 flex flex-col font-medium mt-4 rounded-lg md:space-x-8 rtl:space-x-reverse md:flex-row md:mt-0 md:border-0 md:bg-transparent"
        >
          <li>
            <RouterLink
              to="/"
              class="block py-2 px-3 md:p-0 text-white rounded hover:bg-gray-600 md:hover:bg-transparent"
              >Home</RouterLink
            >
          </li>
          <li>
            <RouterLink
              to="/nosotros"
              class="block py-2 px-3 md:p-0 ounded hover:bg-gray-600 hover:text-white md:hover:bg-transparent"
              >Nosotros</RouterLink
            >
          </li>
          <li>
            <RouterLink
              to="/servicios"
              class="block py-2 px-3 md:p-0 rounded hover:bg-gray-600 hover:text-white md:hover:bg-transparent"
              >Servicios</RouterLink
            >
          </li>
          <li>
            <RouterLink
              to="/espacios"
              class="block py-2 px-3 md:p-0 rounded hover:bg-gray-600 hover:text-white md:hover:bg-transparent"
              >Espacios</RouterLink
            >
          </li>
          <li>
            <button
              data-modal-target="default-modal"
              data-modal-toggle="default-modal"
              type="button"
              class="block py-2 px-3 md:p-0 rounded hover:bg-gray-600 hover:text-white md:hover:bg-transparent"
              sd
            >
              Ingresar
            </button>
          </li>
        </ul>
      </div>
    </div>
  </nav>

  <!-- Main modal -->

  <div
    id="default-modal"
    tabindex="-1"
    aria-hidden="true"
    class="hidden overflow-y-auto overflow-x-hidden fixed top-0 right-0 left-0 z-50 justify-center items-center w-full md:inset-0 h-[calc(100%-1rem)] max-h-full"
  >
    <div
      class="w-full max-w-sm p-4 border border-gray-600 backdrop-blur-lg bg-form rounded-lg shadow sm:p-6 md:p-8"
    >
      <form class="text-white space-y-6" action="#">
        <h5 class="text-xl font-medium">Ingrese a nuestra plataforma</h5>

        <div>
          <label for="email" class="block mb-2 text-sm font-medium"
            >Email</label
          >
          <input
            type="email"
            name="email"
            id="email"
            class="bg-gray-50 border border-gray-300 text-sm rounded-lg focus:ring-blue-500 focus:border-blue-500 block w-full p-2.5 dark:bg-gray-600 dark:border-gray-500 dark:placeholder-gray-400 dark:text-white"
            placeholder="name@company.com"
            required
          />
        </div>
        <div>
          <label
            for="password"
            class="block mb-2 text-sm font-medium dark:text-white"
            >Contraseña</label
          >
          <input
            type="password"
            name="password"
            id="password"
            placeholder="••••••••"
            class="bg-gray-50 border border-gray-300 text-gray-900 text-sm rounded-lg focus:ring-blue-500 focus:border-blue-500 block w-full p-2.5 dark:bg-gray-600 dark:border-gray-500 dark:placeholder-gray-400 dark:text-white"
            required
          />
        </div>
        <div class="flex items-start">
          <div class="flex items-start">
            <div class="flex items-center h-5">
              <input
                id="remember"
                type="checkbox"
                value=""
                class="w-4 h-4 border border-gray-300 rounded bg-gray-50 focus:ring-3 focus:ring-blue-300 dark:bg-gray-700 dark:border-gray-600 dark:focus:ring-blue-600 dark:ring-offset-gray-800 dark:focus:ring-offset-gray-800"
                required
              />
            </div>
            <label for="remember" class="ms-2 text-sm font-medium"
              >Recordar usuario</label
            >
          </div>
          <a href="#" class="ms-auto text-sm text-blue-500 hover:underline"
            >Recuperar contraseña</a
          >
        </div>
        <button
          type="submit"
          class="w-full text-white bg-blue-700 hover:bg-blue-800 focus:ring-4 focus:outline-none focus:ring-blue-300 font-medium rounded-lg text-sm px-5 py-2.5 text-center dark:bg-blue-600 dark:hover:bg-blue-700 dark:focus:ring-blue-800"
        >
          Iniciar sesion
        </button>
        <div class="text-sm font-medium">
          ¿No tienes una cuenta?
          <a href="#" class="text-blue-500 hover:underline"> Regístrate</a>
        </div>
      </form>
    </div>
  </div>
</template>

<script setup>
import { initFlowbite } from "flowbite";
import { onMounted } from "vue";

onMounted(() => {
  initFlowbite();
});
</script>

<style scope>
.bg-form {
  background-color: rgba(23, 23, 23, 0.4);
}
.bg-custom {
  background-color: #23232373;
}
</style>
