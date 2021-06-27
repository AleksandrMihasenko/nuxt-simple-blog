<template>
  <div>
    <div class='py-12 bg-white'>
      <div class='max-w-7xl mx-auto px-4 sm:px-6 lg:px-8'>
        <div class='lg:text-center'>
          <h2 class='text-base text-indigo-600 font-semibold tracking-wide uppercase'>post</h2>
          <p class='mt-4 max-w-2xl text-xl text-gray-500 lg:mx-auto'>
            {{ post.title }}
          </p>
          <p class='mt-2 max-w-2xl text-xl text-gray-500 lg:mx-auto'>Was written by user {{ post.userId }}</p>
        </div>

        <div class='mt-10'>
          <dl class='space-y-5 md:space-y-0 md:grid md:grid-cols-1 md:gap-x-5 md:gap-y-10'>
            <div class='relative'>
              <dd class='mt-2 ml-16 text-base text-gray-500 p-2.5'>
                {{ post.body }}
              </dd>
            </div>
          </dl>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: '_id',
  async asyncData({ $axios, params }) {
    const post = await $axios.$get('https://jsonplaceholder.typicode.com/posts/' + params.id);

    return { post };
  }
}
</script>
