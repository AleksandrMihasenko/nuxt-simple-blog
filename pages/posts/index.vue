<template>
  <div>
    <div class='py-12 bg-white'>
      <div class='max-w-7xl mx-auto px-4 sm:px-6 lg:px-8'>
        <div class='lg:text-center'>
          <h2 class='text-base text-indigo-600 font-semibold tracking-wide uppercase'>All posts</h2>
          <p class='mt-2 text-3xl leading-8 font-extrabold tracking-tight text-gray-900 sm:text-4xl'>
            Read about everything
          </p>
          <p class='mt-4 max-w-2xl text-xl text-gray-500 lg:mx-auto'>
            Lorem ipsum dolor sit amet consect adipisicing elit. Possimus magnam voluptatum cupiditate veritatis in accusamus quisquam.
          </p>
        </div>

        <div class='mt-10'>
          <dl class='space-y-10 md:space-y-0 md:grid md:grid-cols-2 md:gap-x-8 md:gap-y-10'>
            <div v-for='post of 5' :key='post' class='relative'>
              <dd @click='clickHandler(post)' class='mt-2 ml-16 text-base text-gray-500 p-2.5 hover:shadow-md cursor-pointer'>
                Lorem ipsum, dolor sit amet consectetur adipisicing elit. Maiores impedit perferendis suscipit eaque, iste dolor cupiditate blanditiis ratione.
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
  methods: {
    clickHandler (post) {
      this.$router.push('/posts/' + post)
    }
  }
}
</script>
