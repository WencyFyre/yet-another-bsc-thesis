<template>
    <nav
        class="bg-white shadow-md px-6 py-4 flex flex-col md:flex-row items-center md:justify-between gap-4 md:gap-0"
    >
        <!-- Logó / Főoldal link -->
        <router-link to="/" class="text-2xl font-bold text-gray-800 hover:text-blue-600 transition">
            ReceptApp
        </router-link>

        <!-- Kereső -->
        <div class="w-full md:w-1/2">
            <input
                type="text"
                placeholder="Keresés..."
                class="w-full px-4 py-2 border border-gray-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-blue-400"
            />
        </div>

        <!-- Navigáció -->
        <ul class="flex space-x-6 text-gray-700">
            <li><router-link to="/recipes" class="hover:text-blue-600">Receptek</router-link></li>
            <li>
                <router-link to="/new-recipe" class="hover:text-blue-600">Új recept</router-link>
            </li>
            <li><router-link to="/profile" class="hover:text-blue-600">Profil</router-link></li>
        </ul>
    </nav>
</template>
