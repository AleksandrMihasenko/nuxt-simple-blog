<template>
  <nav class='bg-gray-800'>
    <div class='max-w-7xl mx-auto px-2 sm:px-6 lg:px-8'>
      <div class='relative flex items-center justify-between h-16'>
        <div class='absolute inset-y-0 left-0 flex items-center sm:hidden'>
        </div>
        <div class='flex-1 flex items-center justify-center sm:items-stretch sm:justify-start'>
          <div class='flex-shrink-0 flex items-center'>
            <img class='block lg:hidden h-8 w-auto' src='https://tailwindui.com/img/logos/workflow-mark-indigo-500.svg' alt='Workflow'>
            <img class='hidden lg:block h-8 w-auto' src='https://tailwindui.com/img/logos/workflow-logo-indigo-500-mark-white-text.svg' alt='Workflow'>
          </div>
          <div class='hidden sm:block sm:ml-6'>
            <div class='flex space-x-4'>
              <nuxt-link to='/' class='text-gray-300 hover:bg-gray-700 hover:text-white px-3 py-2 rounded-md text-sm font-medium' exact-active-class='bg-gray-900'>Home</nuxt-link>

              <nuxt-link to='/about' class='text-gray-300 hover:bg-gray-700 hover:text-white px-3 py-2 rounded-md text-sm font-medium' exact-active-class='bg-gray-900'>About</nuxt-link>

              <nuxt-link to='/posts' class='text-gray-300 hover:bg-gray-700 hover:text-white px-3 py-2 rounded-md text-sm font-medium' exact-active-class='bg-gray-900'>Posts</nuxt-link>
            </div>
          </div>
        </div>
      </div>
    </div>

    <div class='sm:hidden' id='mobile-menu'>
      <div class='px-2 pt-2 pb-3 space-y-1'>
        <nuxt-link to='/' class='bg-gray-900 text-white block px-3 py-2 rounded-md text-base font-medium'>Home</nuxt-link>

        <nuxt-link to='/about' class='text-gray-300 hover:bg-gray-700 hover:text-white block px-3 py-2 rounded-md text-base font-medium'>About</nuxt-link>

        <nuxt-link to='/posts' class='text-gray-300 hover:bg-gray-700 hover:text-white block px-3 py-2 rounded-md text-base font-medium'>Posts</nuxt-link>
      </div>
    </div>
  </nav>
</template>

<script>
export default {
}
</script>
