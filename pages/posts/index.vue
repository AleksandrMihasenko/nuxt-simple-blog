<template>
  <div>
    <div class='py-12 bg-white'>
      <div class='max-w-7xl mx-auto px-4 sm:px-6 lg:px-8'>
        <div class='lg:text-center'>
          <h2 class='text-base text-indigo-700 font-semibold tracking-wide uppercase'>All posts</h2>
          <p class='mt-2 text-3xl leading-8 font-extrabold tracking-tight text-gray-900 sm:text-4xl'>
            Read about everything
          </p>
          <p class='mt-4 max-w-2xl text-xl text-gray-500 lg:mx-auto'>
            Lorem ipsum dolor sit amet consect adipisicing elit. Possimus magnam voluptatum cupiditate veritatis in accusamus quisquam.
          </p>
        </div>

        <div class='mt-10'>
          <dl class='space-y-10 md:space-y-0 md:grid md:grid-cols-2 md:gap-x-8 md:gap-y-10'>
            <div v-for='post of posts' :key='post.id' class='relative'>
              <dd @click='clickHandler(post)' class='mt-2 ml-16 text-base text-gray-500 p-2.5 h-40 hover:shadow-md cursor-pointer'>
                <h3 class='text-indigo-500 mb-8'>Was written by user {{ post.userId }}</h3>
                {{ post.title }}
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
  name: 'posts',
  async asyncData({ $axios }) {
    const posts = await $axios.$get('https://jsonplaceholder.typicode.com/posts');

    return { posts };
  },
  methods: {
    clickHandler (post) {
      this.$router.push('/posts/' + post.id)
    }
  }
}
</script>
