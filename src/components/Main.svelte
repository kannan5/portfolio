<script>
  import Step from "./Step.svelte";
  let steps = [
    { name: "Pomodoro Timer", icon: "fas fa-stopwatch-20" },
    { name: "The Enigma Machine", icon: "fas fa-brain" },
    { name: "The Ultimate To-Do", icon: "fas fa-list-ol" },
  ];
  let benefits = [
    {
      name: "Passionate Developer",
      description:
        "Passion for crafting cutting-edge solutions that transform ideas into reality. With a robust background in software development, I bring a wealth of experience in designing, implementing, and optimizing complex systems.",
    },
    {
      name: "Backend TechStack",
      description:
        "Majorly Worked on Languages and Backend Technologies Includes Java(Spring Boot, Spring REST API), C#(Core API), Python.",
    },
    {
      name: "Frontend TechStack",
      description:
        "Having Experience On Working Frontend Technologies Inclues ReactJS, Svelte, Angular,JavaScript, TypeScript, HTML, CSS.",
    },
  ];
</script>

<!-- svelte-ignore a11y-invalid-attribute -->
<main class="flex flex-col flex-1 p-4">
  <section
    id="introPage"
    class="grid grid-cols-1 lg:grid-cols-2 gap-10 ру-8 sm:py-14"
  >
    <div
      class="flex flex-col 1g:justify-center text-center lg:text-left gap-6 md:gap-8
            lg:gap-10"
    >
      <h2 class="font-semibold text-4xl sm:text-5xl md:text-6xl">
        Hi! I'm <span class="poppins text-violet-400">Kannan</span> MJ
        <br />Full Stack
        <span class="poppins text-violet-400">Developer</span>
      </h2>
      <p class="text-base sm:text-lg md:text-xl">
        My <span class="text-violet-400">favorite tech</span> includes Spring Boot,
        Sprint REST API, (React or Svelte), .NET Core API, Python, Postgre/MySQL!
      </p>
      <a
        class="blueShadow mx-auto lg:mr-auto lg:ml-0 text-base sm:text-lg md:text-xl poppins
                 relative overflow-hidden px-6 ру-3 group rounded-full bg-white text-slate-950
                cursor-pointer"
        href="#footer"
        style="line-height: 3rem;"
      >
        <div
          class="absolute top-0 right-full w-full h-full bg-violet-400 opacity-20
                    group-hover:translate-x-full z-0 duration-200"
        />
        <h4 class=" relative z-9">Get in touch &rarr;</h4></a
      >
    </div>
    <div class="relative shadow-2xl grid place-items-center">
      <img
        src={"images/profile.png"}
        alt=""
        class="object-cover z-[2] max-h-[70vh]"
      />
    </div>
  </section>
  <section id="projects" class="py-20 lg:py-32 flex flex-col gap-24">
    <div class="flex flex-col gap-2 text-center">
      <h6 class="text-lg sm:text-xl md:text-2xl">
        Few of my creative endeavours.
      </h6>
      <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
        Curious to <span class="poppins text-violet-400">see</span> my work?
      </h3>
    </div>
    <a
      href=""
      target="_blank"
      class="mx-auto px-4 py-2 rounded-md border border-solid border-white flex
        item-center gap-2 -mb-4 sm:-mb-0 -mt-10 hover:border-violet-700 duration-200"
    >
      <i class="fa-regular fa-circle-play self-center"></i>
      <p>Watch The Video</p>
    </a>
    <div class="grid grid-cols-1 lg:grid-cols-3 gap-12 lg:gap-10">
      <Step step={steps[0]}>
        <p>
          Pomodoro Timer Used to Focus on Task and Improve Move Productivity of
          Work. Created using <strong class="text-violet-400"
            >SvelteJs, TypeScript and TailwindCSS.</strong
          >
        </p>
      </Step>
      <Step step={steps[1]}>
        <p>
          The Enigma Machine Inspired from <strong class="text-violet-400"
            >World War 2</strong
          >, The Most Complex Encryption Technology used in Armies. Built using
          <strong class="text-violet-400">
            TypeScript, SvelteJs and TailwindCSS.
          </strong>
        </p>
      </Step>
      <Step step={steps[2]}>
        <p>
          Ultimate To-Do List is a <strong class="text-violet-400"
            >Full Stack Spring Boot + React Js
          </strong>CRUD Application that allows a user to login, manage a tidy
          and efficacious todo list, and persist this information across all
          devices
        </p>
      </Step>
    </div>
  </section>
  <section
    id="about"
    class="py-20 pt-10 lg:pt-16 lg:py-32 flex flex-col gap-16 sm:gap-20 md:gap24 relative"
  >
    <div
      class="flex flex-col gap-2 text-center relative before:absolute before:top-0
     before:left-0 before:w-2/3 before:h-1.5 before:bg-violet-700 after:absolute
  after:bottom-0 after:right-0 after:w-2/3 after:h-1.5 after:bg-violet-700 py-4"
    >
      <h6 class="text-lg sm:text-xl md:text-2xl">Feel Free To Connect</h6>
      <h3 class="">
        A bit <span class="poppins text-violet-400">about</span> Me.
      </h3>
      <p class="mx-auto poppins font-semibold text-lg sm:text-xl md:text-2xl">
        I am . . .
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
    </div>
  </section>
</main>
