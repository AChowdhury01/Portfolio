<script>
  import Step from "./Step.svelte";

  let steps = [
    {
      name: "PathSynapse",
      icon: "fa-solid fa-brain",
      href: "https://github.com/AChowdhury01/PathSynapse",
    },
    {
      name: "Car Rental System",
      icon: "fa-solid fa-car",
      href: "https://github.com/rshah2001/Car_Rental_database_management_system",
    },
    {
      name: "BullIndex",
      icon: "fa-solid fa-chart-line", // Changed icon to be more relevant for a financial tool
      href: "https://github.com/AChowdhury01/BullIndex", // Update with actual repo URL
    },
  ];

  let benefits = [
    {
      metric: "10x",
      name: "a skilled software developer",
      description:
        "With a strong foundation in Python, C, C++, and SQL, I've developed expertise in creating efficient and scalable solutions. My experience with frameworks like Flask and libraries such as Pandas and NumPy enables me to build robust applications and perform complex data operations.",
    },
    {
      name: "a technical problem solver",
      description:
        "I excel in algorithmic thinking and data structures, allowing me to tackle complex technical challenges effectively. My experience with API Integration and various programming languages helps me create comprehensive solutions that meet modern development needs.",
    },
    {
      name: "a collaborative team player",
      description:
        "Using tools like Git and GitHub, I've developed strong version control skills that enable effective collaboration. I believe in writing clean, maintainable code and working together with team members to achieve project goals efficiently.",
    },
  ];
</script>

<main class="flex flex-col flex-1 p-4">
  <section id="introPage" class="grid lg:grid-cols-2 gap-10 py-8 md:px-14">
    <div
      class="flex flex-col lg:justify-center text-center lg:text-left gap-6 md:gap-8 lg:gap-10"
    >
      <h2 class="font-semibold text-4xl sm:text-5xl md:text-6xl">
        Hi! I'm <span class="poppins text-cyan-400">Ashfak</span> Chowdhury
        <br />Full Stack
        <span class="poppins text-cyan-400">Developer</span>
      </h2>
      <p class="text-base sm:text-xl md:text-2xl">
        My <span class="text-cyan-400">favorite tech</span> includes Python, Flask,
        Pandas, NumPy, and SQL. I'm passionate about creating efficient solutions
        using data structures and algorithms!
      </p>
      <a
        href="mailto:ash.chy009@gmail.com"
        target="_blank"
        class="blueShadow mx-auto lg:mr-auto lg:ml-0 relative overflow-hidden px-7 py-3 group rounded-full bg-white text-zinc-950"
      >
        <div
          class="absolute top-0 right-full w-full h-full bg-cyan-400 opacity-20 group-hover:translate-x-full z-0 duration-300"
        ></div>
        <h4 class="relative text-xl z-9">Get in touch &rarr;</h4>
      </a>
    </div>

    <div class="z-[0]">
      <img
        style="filter: drop-shadow(5 0 5px #0d9488)"
        class="shadow-4xl grayscale-[85%] hover:grayscale-[0%] rounded-[20px] duration-700"
        src="./assets/Ashfak.jpg"
        alt=" "
      />
    </div>
  </section>

  <section id="projects" class="py-16 flex flex-col gap-24">
    <div class="flex flex-col gap-2 text-center">
      <h6 class="text-lg sm:text-xl md:text-2xl">
        A few of my creative endeavours
      </h6>
      <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
        Curious to <span class="poppins text-cyan-400">see</span> my works?
      </h3>
    </div>
    <div class="grid grid-cols-1 lg:grid-cols-2 gap-12 lg:gap-10">
      <Step step={steps[0]}>
        <p>
          PathSynapse is an engaging brain-training game built with <strong
            class="text-cyan-400">Python</strong
          >. Test your numerical knowledge and problem-solving skills through an
          interactive number grid game that challenges your cognitive abilities.
        </p>
      </Step>
      <Step step={steps[1]}>
        <p>
          A comprehensive Car Rental System developed with <strong
            class="text-cyan-400">Python, PostgreSQL, and Streamlit</strong
          >. Features a user-friendly interface for managing rentals, customer
          data, and inventory tracking with a robust database backend.
        </p>
      </Step>
      <Step step={steps[2]}>
        <p>
          BullIndex is a sophisticated stock analysis tool built with <strong
            class="text-cyan-400"
            >C++, Windows Forms, and Chart Visualization</strong
          >. Features include candlestick pattern analysis, smart chart
          visualization, and wave selection algorithms for technical analysis.
          Developed in Visual Studio using advanced data visualization
          libraries.
        </p>
      </Step>
    </div>
  </section>

  <section
    id="about"
    class="py-20 pt-10 lg:pt-16 lg:py-32 flex flex-col gap-16 sm:gap-12 md:gap-14"
  >
    <div class="flex flex-col gap-2 text-center relative py-8">
      <h6 class="text-lg sm:text-xl md:text-2xl">Want to know more?</h6>
      <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
        A bit <span class="poppins text-cyan-400">about</span> me.
      </h3>
    </div>
    <p class="mx-auto poppins font-semibold text-lg sm:text-xl md:text-2xl">
      I am . . .
    </p>
    <div class="flex flex-col gap-20 w-[60%] mx-auto maz-w-[800px]">
      {#each benefits as benefit, index}
        <div class="flex gap-6 sm:gap-8">
          <p
            class="poppins text-4xl sm:text-5xl md:text-6xl text-zinc-500 font-semibold"
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
    <div class="mx-auto -mt-12 italic sm:hidden opacity-50">
      <p>Scroll to see more &rarr;</p>
    </div>
  </section>
</main>
