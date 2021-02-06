<template>
  <div class="dark:bg-gray-900 overflow-x-hidden">
    <!--Hero-->
    <div style="margin-top: -182px">
      <div
        class="container px-3 mx-auto flex flex-wrap flex-col md:flex-row items-center"
      >
        <!--Left Col-->
        <div
          class="flex flex-col mt-48 w-full pt-48 md:w-2/5 justify-center items-start text-center md:text-left"
        >
          <p class="uppercase tracking-loose w-full select-none pl-1">
            Design | Development | DevOps | Testing
          </p>
          <h1
            class="mb-4 text-5xl font-bold leading-tight text-gray-900 dark:text-white select-none"
          >
            Software Development Redefined.
          </h1>
          <p
            class="leading-normal text-2xl mb-8 text-gray-900 dark:text-white select-none"
          >
            With end-to-end solutions for all your needs, Turinc offers
            professionally vetted developers from around the globe, that too
            on-demand!
          </p>
        </div>
        <!--Right Col-->
        <div
          class="flex flex-col w-full md:w-3/5 justify center items-start text-center md:text-right"
        >
          <lottie
            :width="1024"
            :height="1024"
            :options="lottieOptions"
            v-on:animCreated="handleAnimation"
          />
        </div>
      </div>
    </div>
    <div class="bg-gray-100" style="margin-top: -176px">
      <div class="container mx-auto px-6 pt-4 pb-12 text-gray-900">
        <h1
          class="w-full my-2 text-5xl font-bold leading-tight text-center text-gray-900 select-none"
        >
          Our ever-growing technology stack
        </h1>
        <div class="card-container mt-24">
          <div
            class="card bg-white rounded-3xl flex flex-col w-5/6 lg:w-1/4 mx-auto lg:mx-0 rounded-none lg:rounded-l-lg bg-white mt-0"
            v-for="dept in technologies"
            :key="dept.id"
          >
            <div
              class="flex-1 bg-white text-gray-900 rounded-t rounded-b-none overflow-hidden shadow"
            >
              <div
                class="p-8 text-3xl font-bold text-center border-b-4 select-none"
              >
                {{ dept.name }}
              </div>
              <ul class="w-full text-center text-sm">
                <li
                  class="border-b py-4 transition duration-500 transform hover:scale-125 select-none ease-in-out"
                  v-for="tech in dept.technologies"
                  :key="tech"
                >
                  {{ tech }}
                </li>
              </ul>
            </div>
          </div>
        </div>
      </div>
    </div>
    <!-- Change the colour #f8fafc to match the previous section colour -->
    <svg
      class="wave-top"
      viewBox="0 0 1439 147"
      version="1.1"
      xmlns="http://www.w3.org/2000/svg"
      xmlns:xlink="http://www.w3.org/1999/xlink"
    >
      <g stroke="none" stroke-width="1" fill="none" fill-rule="evenodd">
        <g transform="translate(-1.000000, -14.000000)" fill-rule="nonzero">
          <g class="wave" fill="#f8fafc">
            <path
              d="M1440,84 C1383.555,64.3 1342.555,51.3 1317,45 C1259.5,30.824 1206.707,25.526 1169,22 C1129.711,18.326 1044.426,18.475 980,22 C954.25,23.409 922.25,26.742 884,32 C845.122,37.787 818.455,42.121 804,45 C776.833,50.41 728.136,61.77 713,65 C660.023,76.309 621.544,87.729 584,94 C517.525,105.104 484.525,106.438 429,108 C379.49,106.484 342.823,104.484 319,102 C278.571,97.783 231.737,88.736 205,84 C154.629,75.076 86.296,57.743 0,32 L0,0 L1440,0 L1440,84 Z"
            ></path>
          </g>
          <g transform="translate(1.000000, 15.000000)" fill="#FFFFFF">
            <g
              transform="translate(719.500000, 68.500000) rotate(-180.000000) translate(-719.500000, -68.500000) "
            >
              <path
                d="M0,0 C90.7283404,0.927527913 147.912752,27.187927 291.910178,59.9119003 C387.908462,81.7278826 543.605069,89.334785 759,82.7326078 C469.336065,156.254352 216.336065,153.6679 0,74.9732496"
                opacity="0.100000001"
              ></path>
              <path
                d="M100,104.708498 C277.413333,72.2345949 426.147877,52.5246657 546.203633,45.5787101 C666.259389,38.6327546 810.524845,41.7979068 979,55.0741668 C931.069965,56.122511 810.303266,74.8455141 616.699903,111.243176 C423.096539,147.640838 250.863238,145.462612 100,104.708498 Z"
                opacity="0.100000001"
              ></path>
              <path
                d="M1046,51.6521276 C1130.83045,29.328812 1279.08318,17.607883 1439,40.1656806 L1439,120 C1271.17211,77.9435312 1140.17211,55.1609071 1046,51.6521276 Z"
                opacity="0.200000003"
              ></path>
            </g>
          </g>
        </g>
      </g>
    </svg>
    <div class="container mx-auto text-center py-6 mb-12">
      <h3 class="my-4 text-3xl leading-tight">
        To get started on your latest project, contact us today!
      </h3>
      <Button
        text="Contact us"
        classes="m-3 py-4 px-8 bg-gray-900 dark:bg-white dark:text-gray-900 text-white outline-none transition duration-500 ease-in-out transform hover:scale-105 rounded-md"
      />
    </div>
    <!--Footer-->
  </div>
</template>
<script>
if (process.browser) {
  let scrollpos = window.scrollY;
  let header = document.getElementById("header");
  let navcontent = document.getElementById("nav-content");
  let navaction = document.getElementById("navAction");
  let brandname = document.getElementById("brandname");
  let toToggle = document.querySelectorAll(".toggleColour");

  document.addEventListener("scroll", function () {
    /*Apply classes for slide in bar*/
    scrollpos = window.scrollY;

    if (scrollpos > 10) {
      header.classList.add("bg-white");
      navaction.classList.remove("bg-white");
      navaction.classList.add("gradient");
      navaction.classList.remove("text-gray-900");
      navaction.classList.add("text-white");
      //Use to switch toggleColour colours
      for (let i = 0; i < toToggle.length; i++) {
        toToggle[i].classList.add("text-gray-900");
        toToggle[i].classList.remove("text-white");
      }
      header.classList.add("shadow");
      navcontent.classList.remove("bg-gray-100");
      navcontent.classList.add("bg-white");
    } else {
      header.classList.remove("bg-white");
      navaction.classList.remove("gradient");
      navaction.classList.add("bg-white");
      navaction.classList.remove("text-white");
      navaction.classList.add("text-gray-900");
      //Use to switch toggleColour colours
      for (let i = 0; i < toToggle.length; i++) {
        toToggle[i].classList.add("text-white");
        toToggle[i].classList.remove("text-gray-900");
      }

      header.classList.remove("shadow");
      navcontent.classList.remove("bg-white");
      navcontent.classList.add("bg-gray-100");
    }
  });
  /*Toggle dropdown list*/
  /*https://gist.github.com/slavapas/593e8e50cf4cc16ac972afcbad4f70c8*/

  let navMenuDiv = document.getElementById("nav-content");
  let navMenu = document.getElementById("nav-toggle");

  document.onclick = check;
  function check(e) {
    let target = (e && e.target) || (event && event.srcElement);

    //Nav Menu
    if (!checkParent(target, navMenuDiv)) {
      // click NOT on the menu
      if (checkParent(target, navMenu)) {
        // click on the link
        if (navMenuDiv.classList.contains("hidden")) {
          navMenuDiv.classList.remove("hidden");
        } else {
          navMenuDiv.classList.add("hidden");
        }
      } else {
        // click both outside link and outside menu, hide menu
        navMenuDiv.classList.add("hidden");
      }
    }
  }
  function checkParent(t, elm) {
    while (t.parentNode) {
      if (t == elm) {
        return true;
      }
      t = t.parentNode;
    }
    return false;
  }
}
import lottie from "vue-lottie/src/lottie.vue";
import * as animationData from "~/assets/Animations/developer-animation.json";
import Logo from "@/components/Logo";
export default {
  components: {
    lottie,
    Logo,
  },
  data() {
    return {
      anim: null, // for saving the reference to the animation
      lottieOptions: { animationData: animationData.default },
      technologies: [
        {
          id: 1,
          name: "UI/UX",
          technologies: [
            "Adobe Photoshop",
            "Adobe XD",
            "Figma",
            "Sketch",
            "Zeplin",
          ],
        },
        {
          id: 2,
          name: "Front-End",
          technologies: [
            "Javascript",
            "Typescript",
            "Angular",
            "React",
            "Vue.js",
            "Nuxt.js",
            "Django",
          ],
        },
        {
          id: 3,
          name: "Back-End",
          technologies: [
            "Node.js",
            "Express.js",
            "Java",
            "Springboot",
            "C#",
            ".NET Core",
            "Python",
          ],
        },
        {
          id: 4,
          name: "Version Control",
          technologies: ["Git", "GitHub", "BitBucket", "SVN"],
        },
        {
          id: 5,
          name: "DevOps",
          technologies: [
            "AWS",
            "Kubernetes",
            "Azure",
            "Serverless",
            "Digital Ocean",
          ],
        },
        // {
        //   id: 6,
        //   name: "Testing",
        //   technologies: [""]
        // },
      ],
    };
  },
  methods: {
    handleAnimation: function (anim) {
      this.anim = anim;
    },
  },
};
</script>
<style scoped>
.card-container {
  height: 500px;
  width: inherit;
  display: flex;
  justify-content: center;
}

.card {
  transition: 0.6s ease-out;
  position: relative;
}

.card:not(:first-child) {
  margin-left: -50px;
}

.card:hover {
  transform: translateY(-20px);
  transition: 0.4s ease-out;
}

.card:hover ~ .card {
  position: relative;
  left: 50px;
  transition: 0.4s ease-out;
}

.title {
  color: white;
  font-weight: 300;
  position: absolute;
  left: 20px;
  top: 15px;
}

.bar {
  position: absolute;
  top: 100px;
  left: 20px;
  height: 5px;
  width: 150px;
}

.emptybar {
  background-color: #2e3033;
  width: 100%;
  height: 100%;
}

.filledbar {
  position: absolute;
  top: 0px;
  z-index: 3;
  width: 0px;
  height: 100%;
  background: rgb(0, 154, 217);
  background: linear-gradient(
    90deg,
    rgba(0, 154, 217, 1) 0%,
    rgba(217, 147, 0, 1) 65%,
    rgba(255, 186, 0, 1) 100%
  );
  transition: 0.6s ease-out;
}

.card:hover .filledbar {
  width: 120px;
  transition: 0.4s ease-out;
}

.circle {
  position: absolute;
  top: 150px;
  left: calc(50% - 60px);
}

.stroke {
  stroke: white;
  stroke-dasharray: 360;
  stroke-dashoffset: 360;
  transition: 0.6s ease-out;
}

svg {
  fill: #17141d;
  stroke-width: 2px;
}

.card:hover .stroke {
  stroke-dashoffset: 100;
  transition: 0.6s ease-out;
}
</style>
