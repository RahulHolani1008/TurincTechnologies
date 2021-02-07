<template>
  <div class="dark:bg-gray-900 overflow-x-hidden">
    <div
      class="container px-3 mx-auto flex flex-wrap flex-col md:flex-row items-center"
    >
      <h1
        class="w-full my-2 text-5xl font-bold leading-tight text-center text-gray-900 select-none"
      >
        Humble Beginnings
      </h1>
      <p
        class="mx-auto w-3/5 my-2 text-md leading-tight text-center text-gray-900 select-none"
      >
        Starting off in a small town in India, Turinc quickly grew, gaining the
        trust of a lot of clients through our developers' technical skills and
        unwaivering interest in making the best possible product for our
        clients, as though it was their own. Soon expanding to Chicago and
        Bangalore, Turinc turned into the multi-national corporation the it is
        today.
      </p>
    </div>
    <div
      class="container px-3 mx-auto flex flex-wrap flex-col md:flex-row items-center"
    >
      <h1
        class="w-full my-2 text-5xl font-bold leading-tight text-center text-gray-900 select-none"
      >
        About the developers
      </h1>
      <div
        class="mx-auto w-3/5 my-2 text-md leading-tight text-center text-gray-900 select-none flex justify-around"
      >
        <div
          class="card bg-white rounded-3xl flex flex-col w-5/6 lg:w-1/3 mx-auto lg:mx-0 rounded-none lg:rounded-l-lg bg-white mt-0"
          v-for="developer in developers"
          :key="developer.name"
        >
          <div
            class="flex-1 bg-white text-gray-900 rounded-t rounded-b-none overflow-hidden shadow"
          >
            <div
              class="p-8 text-3xl font-bold text-center border-b-4 select-none"
            >
              <img
                :src="
                  require('@/assets/Images/' + developer.imageName + '.jpg')
                "
                class="rounded-full h-48 w-48 flex items-center object-cover object-top ml-2 mb-2 transition duration-500 transform hover:scale-105 select-none ease-in-out"
              />
              {{ developer.name }}
            </div>
            <!-- <ul class="w-full text-center text-sm">
                <li
                  class="border-b py-4 transition duration-500 transform hover:scale-125 select-none ease-in-out"
                >
                  {{ tech }}
                </li>
              </ul> -->
            <p class="py-4 w-5/6 mx-auto">
              {{ developer.description }}
            </p>
            <div class="py-4">
              <p>Currently Located in</p>
              <p>{{ developer.currentlyLocated }}</p>
            </div>
            <div class="py-2">
              <a :href="developer.linkedin">Linkedin</a>
            </div>
            <div class="py-2">
              <a :href="developer.github">GitHub</a>
            </div>
            <div class="py-2">
              <a :href="developer.upwork">Upwork</a>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      developers: [
        {
          name: "Rahul Holani",
          imageName: "RahulHolani",
          description:
            "Our Lead developer and CEO, Rahul has immense experience in a professional environment. He expertises in solution architecture and ideation. His skills as a developer are no less, writing extremely modular and performance efficient code in the quickest of times.",
          linkedin: "https://www.linkedin.com/in/rahulholani/",
          github: "https://www.github.com/RahulHolani1008/",
          upwork: "https://www.upwork.com/freelancers/~01a328535a8292ca18",
          currentlyLocated: "Chicago",
        },
        {
          name: "Sanjay Krishnan",
          imageName: "SanjayKrishnan",
          description: "He is what you call, 'a lodu'",
          linkedin: "https://www.linkedin.com/in/rahulholani/",
          github: "https://www.github.com/RahulHolani1008/",
          upwork: "https://www.upwork.com/freelancers/~01a328535a8292ca18",
          currentlyLocated: "Bangalore",
        },
      ],
    };
  },
};
</script>