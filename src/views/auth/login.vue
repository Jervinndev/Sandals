<template>
    <section class="flex min-h-screen items-center justify-center p-5">
        <div class="w-full max-w-md rounded-2xl border border-black/10 bg-white p-6 sm:p-6">
            <div class="mb-6 text-center">
                <h1 class="font-outfit text-2xl font-bold text-[#3C3C3C]">Welcome back</h1>
                <p class="mt-2 text-sm text-[#5B5B5B]">Log in to continue shopping with Solei &amp; Co.</p>
            </div>

            <form class="flex flex-col gap-4">
                <div class="flex flex-col gap-1.5">
                    <label for="email" class="text-sm font-medium text-[#3C3C3C]">Email address</label>
                    <input id="email" name="email" type="email" autocomplete="email" required
                        placeholder="you@example.com"
                        class="w-full rounded-lg border border-gray-200 bg-gray-100 p-2 outline-none focus:ring-2 focus:ring-orange-400">
                </div>

                <div class="flex flex-col gap-1.5">
                    <label for="password" class="text-sm font-medium text-[#3C3C3C]">Password</label>
                    <input id="password" name="password" type="password" autocomplete="current-password" required
                        placeholder="Enter your password"
                        class="w-full rounded-lg border border-gray-200 bg-gray-100 p-2 outline-none focus:ring-2 focus:ring-orange-400">
                </div>

                <button type="submit"
                    class="mt-1 w-full rounded-lg bg-orange-400 p-2 font-outfit font-semibold text-white transition-colors hover:bg-orange-500 focus:outline-none focus:ring-2 focus:ring-orange-400 focus:ring-offset-2">
                    Log in
                </button>
            </form>

            <p class="mt-6 text-center text-sm text-[#5B5B5B]">
                Don't have an account?
                <router-link to="/Register"
                    class="font-semibold text-orange-500 hover:text-orange-600">Register</router-link>
            </p>
        </div>
    </section>
</template>