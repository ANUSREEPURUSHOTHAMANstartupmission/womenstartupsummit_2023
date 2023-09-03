<script>
    import {onMount} from 'svelte';
  
    let speaker_list = [];
  
    onMount(()=>{
      fetch(`https://events.startupmission.in/api/event/wss-2023/speakers?category=speaker`)
          .then(response => response.json())
          .then((json) => {
            speaker_list = json;
          });
    });
  
  </script>
  
  {#each Object.entries(speaker_list) as [category, speakers]}

    <div class="mx-auto speakers__container ">
  
      <div class="grid grid-cols-2 md:grid-cols-4 sm:grid-cols-3">
        {#each speakers as {name, designation, organisation, photo, linkedin}}
       <div class=" flex flex-col mb-5">
        <div class="relative group mb-2">
            <img src="{photo}" alt="Your Image" class="w-full md:h-96 h-auto" />
            <div class="hidden group-hover:flex group-hover:flex-col absolute top-0 left-0 w-full h-full text-center group-hover:mx-auto group-hover:my-auto bg-black bg-opacity-75  transition-opacity duration-300 flex justify-center items-center">
             
            <p class="text-white text-lg font-sans font-semibold">{designation}</p>
              <p class="text-white text-base">{organisation}</p>


            </div>
        </div>
        <p class="text-white text-lg text-center">{name}</p>

       </div>
       
        {/each}
      </div>
  
    </div>
  {/each}
  