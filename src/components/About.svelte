<script>
  import {scale, fly, fade, blur, slide} from 'svelte/transition'
</script>

<section id="about" class="text-gray-600 body-font" >
  <div class="container mx-auto flex px-5 py-24 md:flex-row flex-col items-center">
    <div class="lg:max-w-lg lg:w-full md:w-1/2 w-5/6 mb-10 md:mb-0">
      <img in:blur={{duration:1500}} class="object-cover object-center rounded" alt="hero" src="/images/IMG_4447.JPG">
    </div>
    <div class="lg:flex-grow md:w-1/2 lg:pl-24 md:pl-16 flex flex-col md:items-start md:text-left items-center text-center">
      <h1 in:fly={{x:100, duration:500}} class="title-font sm:text-4xl text-3xl mb-4 font-medium text-gray-900">Hi! My name is Helena Zarazua
        <br class="hidden lg:inline-block">
      </h1>
      <p in:fly={{x:100, delay:500, duration:500}} class="mb-8 leading-relaxed">I'm a Full Stack Software Engineer based in San Francisco. I love using programming as a creative outlet and making beautiful apps that are engaging and easy to use, I really enjoy the logical challenges of coming up with innovative functionality/features that really make a project stand out and I thrive in a collaborative and social environment.</p>
      <div in:fly={{x:100,  delay:1000, duration:500}} class="flex justify-center">
        <a target="blank" href="https://www.linkedin.com/in/helena-zarazua-50b7a3127/" class="devicon-linkedin-plain colored mr-5 text-5xl"></a>
        <a target="blank" href="https://github.com/Helenasky93" class="devicon-github-original colored text-5xl"></a>
      </div>
    </div>
  </div>
</section>