<script>
  import Step from "./Step.svelte"

  let steps = [
    { name: "EasyML", icon: "fa-soild fa-cart-shopping" },
    { name: "Secure data training", icon: "fa-solid fa-list-check" },
    { name: "The future is here", icon: "fa-soild fa-diagram-project" },
  ]

  let benefits = [
    {
      name: "Your privacy is heavily regulated and we are GDPR compliant",
      description: "Your precious data is safer with us",
    },
    {
      name: "We are on the cutting edge of ML tech",
      description:
        "We utilise the latest technologies in our product so you can reap the most benefits",
    },
    {
      name: "We are here for you, contact us today",
      description: "We have agents ready to assist you whenever you need it",
    },
  ]
</script>

<main class="flex flex-col flex-1 p-4">
  <section
    id="introPage"
    class="grid grid-cols-1 lg:grid-cols-2 gap-10 py-8 sm:py-14"
  >
    <div
      class="flex flex-col lg:justify-center text-center lg:text-left gap-6 md:gap-8 lg:gap-10"
    >
      <h2 class="font-semibold text-4xl sm:text-5xl md:tex5-6xl">
        This is <span class="poppins text-violet-400">EasyML</span>
        <br />The only Machine Learning platform designed for
        <span class="poppins text-violet-400">everyone</span>
      </h2>
      <p class="text-base sm:text-lg md:text-xl">
        We designed our platform from the <span class="text-violet-400"
          >ground up</span
        > to facilitate Machine Learning access to the world
      </p>

      <!-- This 'a' creates a flexible white placeholder for a new button -->
      <!-- Add the link to the application page maybe here -->
      <a
        class="blueShadow mx-auto lg:mr-auto text-base sm:text-lg md:text-cl poppins relative overflow-hidden px-6 py-3 group rounded-full bg-white text-slate-950 cursor-pointer"
        href="#"
        target="_blank"
      >
        <div
          class="absolute top-0 right-full w-full h-full bg-violet-400 opacity-20 group-hover:translate-x-full z-0 duration-200"
        ></div>
        <h4 class="relative z-9">Get started now &rarr;</h4>
      </a>
    </div>
    <div class="relative shadow-2xl grid place-items-center">
      <img
        src={"images/Profile.png"}
        alt="Profile image"
        class="object-cover z-[2] max-h-[30vh]"
      />
    </div>
  </section>

  <section id="projects" class="py-20 lg:py-32 flex flex-col gap-24">
    <div class="flex flex-col gap-2 text-center">
      <h6 class="text-lg sm:text-xl md:text-2xl">
        Curious? Keep reading below
      </h6>
      <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
        What is the <span class="poppins text-violet-400">Machine Learning</span
        > craze about anyway?
      </h3>
    </div>
    <!-- mx-auto = margin on the x axis auto, px-4 = padding on the x axis 4, py-2 = padding on the y axis 2 -->
    <a
      href="https://www.youtube.com/watch?v=PeMlggyqz0Y"
      target="_blank"
      class="mx-auto px-4 py-2 rounded-md border border-solid border-white flex items-center gap-2 -mb-4 sm:-mb-0 -mt-10 hover:border-violet-700 duration-200"
    >
      <i class="fa-regular fa-circle-play"></i>
      <p>Watch this video</p>
    </a>
    <div class="grid grid-cols-1 lg:grid-cols-3 gap-12 lg:gap-10">
      <Step step={steps[0]}>
        <p>
          EasyML is the only platform currently available that creates machine
          learning opportunities for users with their <strong
            class="text-violet-400">own datasets.</strong
          >
        </p>
      </Step>
      <Step step={steps[1]}>
        <p>
          Does your organisation have extensive stores of data that could be
          utilised for training? You can train your own machine learning model
          with that data <strong class="text-violet-400">securely.</strong>
        </p>
      </Step>
      <Step step={steps[2]}>
        <p>
          No other service can guarantee the goverenace of your data through
          their training services. EasyML can make that guarantee. After all we
          are <strong class="text-violet-400">GDPR complaint.</strong>
        </p>
      </Step>
    </div>
  </section>
  <section
    id="about"
    class="py-20 pt-10 lg:pt-16 lg:py-32 flex flex-col gap-16 sm:gap-20 md:gap-24 relative"
  >
    <div
      class="flex flex-col gap-2 text-center relative before:absolute before:top-0 before:left-0 before:w-2/3 before:h-1.5 before:bg-violet-700 after:absolute after:bottom-0 after:right-0 after:w-2/3 after:h-1.5 after:bg-violet-700 py-4"
    >
      <h6 class="text-lg sm:text-xl md:text-2xl">Want to know even more?</h6>
      <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
        A bit <span class="poppins text-violet-400">about</span> us.
      </h3>
    </div>
    <p class="mx-auto poppins font-semibold text-lg sm:text-xl md:text-2xl">
      Easy ML is well known for these features
    </p>
    <div class="flex flex-col gap-20 w-full mx-auto max-w-[800px]">
      {#each benefits as benefit, index}
        <div class="flex gap-6 sm:gap-8">
          <p
            class="poppins text-4xl sm:text-5xl md:text-6xl text-slate-500 font-semibold"
          >
            0{index + 1}
          </p>
          <div class="flex flex-col gap-6 sm:gap-8">
            <h3 class="text-2xl sm:text-3xl md:text-5xl">
              {benefit.name}
            </h3>
            <p>{benefit.description}</p>
          </div>
        </div>
      {/each}
    </div>
    <h5 class="text-2xl sm:text-3xl font-semibold text-center poppins">
      The <span class="text-violet-400 poppins">Complete</span> ML Package
    </h5>
    <div
      class="flex flex-col overflow-x-scroll gap-10 max-w-[800px] mx-auto w-full"
    >
      <table class="bg-white text-slate-700 rounded text-center">
        <thead class="border-b border-solid border-slate-200">
          <tr class="">
            <th />
            <th class="whitespace-nowrap p-2 px-4">Competitor #1</th>
            <th class="whitespace-nowrap p-2 px-4">Competitor #2</th>
            <th class="whitespace-nowrap p-2 px-4">Competitor #3</th>
            <th class="whitespace-nowrap bg-violet-700 text-white p-4 px-8"
              >EasyML</th
            >
          </tr>
        </thead>
        <tbody>
          <tr class="border-b border-solid border-slate-200">
            <td
              class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold text-sm whitespace-nowrap"
              >Easy to Configure</td
            >
            <td><i class="fa-solid fa-xmark text-slate-500"></i></td>
            <td><i class="fa-solid fa-xmark text-slate-500"></i></td>
            <td><i class="fa-solid fa-xmark text-slate-500"></i></td>
            <td><i class="fa-solid fa-check text-green-500"></i></td>
          </tr>
          <tr class="border-b border-solid border-slate-200">
            <td
              class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold text-sm whitespace-nowrap"
              >Next-Gen Architecture</td
            >
            <td><i class="fa-solid fa-check text-slate-500"></i></td>
            <td><i class="fa-solid fa-xmark text-slate-500"></i></td>
            <td><i class="fa-solid fa-xmark text-slate-500"></i></td>
            <td><i class="fa-solid fa-check text-green-500"></i></td>
          </tr>
          <tr class="border-b border-solid border-slate-200">
            <td
              class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold text-sm whitespace-nowrap"
              >GDPR Compliant</td
            >
            <td><i class="fa-solid fa-xmark text-slate-500"></i></td>
            <td><i class="fa-solid fa-check text-slate-500"></i></td>
            <td><i class="fa-solid fa-xmark text-slate-500"></i></td>
            <td><i class="fa-solid fa-check text-green-500"></i></td>
          </tr>
          <tr class="border-b border-solid border-slate-200">
            <td
              class="border-r border-solid border-white pl-4 pr-8 py-4 font-semibold text-sm whitespace-nowrap"
              >Future Orientated</td
            >
            <td><i class="fa-solid fa-xmark text-slate-500"></i></td>
            <td><i class="fa-solid fa-xmark text-slate-500"></i></td>
            <td><i class="fa-solid fa-xmark text-slate-500"></i></td>
            <td><i class="fa-solid fa-check text-green-500"></i></td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="mx-auto -mt-12 italic sm:hidden opacity-50">
      <p>Scroll to see more &rarr;</p>
    </div>
    <p class="mx-auto">So what are you waiting for? Start today</p>
  </section>
</main>
