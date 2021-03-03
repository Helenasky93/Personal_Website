<script>
  import {flip} from 'svelte/animate';
  const topSkills = [
'devicon-ruby-plain-wordmark',
'devicon-rails-plain-wordmark',
'devicon-react-original-wordmark',
'devicon-redux-original',
'devicon-javascript-plain',
'devicon-nodejs-plain',
'devicon-jquery-plain-wordmark',
'devicon-postgresql-plain-wordmark',
'devicon-html5-plain-wordmark',
'devicon-css3-plain-wordmark',
'devicon-git-plain-wordmark',
'devicon-amazonwebservices-plain-wordmark',
'devicon-mongodb-plain-wordmark',
'devicon-heroku-plain-wordmark',]

  let skills = [...topSkills]
  let sortedBy = 'top';

function alphabetize() {
  skills = skills.sort();
  sortedBy = 'alpha';
}
function topSkillsSort() {
  skills = [...topSkills];
  sortedBy = 'top';
}

</script>

<section id="skills" class="text-gray-600 body-font">
  <div class="container px-5 py-24 mx-auto">
    <div class="flex flex-col text-center w-full mb-20">
      <h1 class="sm:text-3xl text-2xl font-medium title-font mb-4 text-gray-900">Skills</h1>
      <div class="flex justify-center">

        <button class="flex  text-black border-0 py-2 px-8 focus:outline-none hover:bg-purple-600 rounded text-lg"
        class:bg-gray-100={sortedBy !== 'alpha'}
        class:bg-purple-500={sortedBy === 'alpha'}
        class:text-black={sortedBy !== 'alpha'}
        class:text-white={sortedBy === 'alpha'} 
         on:click={alphabetize}>Sort alphabetically</button>
        <button class="flex ml-5 text-black border-0 py-2 px-8 focus:outline-none hover:bg-purple-600 rounded text-lg"
        class:bg-gray-100={sortedBy !== 'top'}
        class:bg-purple-500={sortedBy === 'top'}
        class:text-black={sortedBy !== 'top'}
        class:text-white={sortedBy === 'top'}
         on:click={topSkillsSort}>Sort by top skills</button>
      </div>
    </div>
    <div class="flex flex-wrap -m-2">
      {#each skills as skill (skill)}
      <div class="p-2 lg:w-1/4 md:w-1/2 w-full" animate:flip={{duration:500}} >
        <div class="h-full flex justify-center" >
          <i class="{skill} colored text-8xl"></i>
        </div>
      </div>
      {/each}
      
    </div>
  </div>
</section>