<template>
  <div class="portfolio">
    <Title badge="PORTFOLIO" text="Creative Portfolio" />

    <div class="d-flex justify-content-end w-100 filter-content">
      <div
        v-for="tab in tabs"
        class="mx-2 px-3 py-1 tab-btn rounded"
        :class="selectedTab === tab.slug ? 'active' : ''"
        :key="tab.name"
        @click="selectTab(tab.slug)"
      >
        {{ tab.name }}
      </div>
    </div>
    <div class="container mt-4">
      <div class="row mb-3">
        <div
          class="col-xl-4 col-md-6 col-12 mt-3"
          v-for="site in filterSites()"
          :key="site.link"
        >
          <PortfolioCard :site="site" />
        </div>
      </div>
    </div>
  </div>
</template>
<script>
import "./style.css";
import { Title } from "../../ui-components";
import PortfolioCard from "../PortfolioCard/PortfolioCard.vue";
export default {
  data() {
    return {
      selectedTab: "all",
      tabs: [
        {
          id: 1,
          name: "All",
          slug: "all",
        },

        {
          id: 2,
          name: "React",
          slug: "react",
        },
        {
          id: 3,
          name: "Vue",
          slug: "vue",
        },
        {
          id: 4,
          name: "HTML/CSS",
          slug: "html",
        },
      ],
      sites: [
        {
          id: 4,
          title: "Houzing",
          image: "/assets/img/housing.PNG",
          stacks: [
            "React",
            "Context API",
            "Styled-Components",
            "AntD",
            "Backend",
          ],
          link: "https://housing-neon.vercel.app/home",
          tab: "react",
        },
        {
          id: 5,
          title: "Article",
          image: "/assets/img/article.PNG",
          stacks: ["Vue", "Vuex", "Bootstrap", "Backend", "CRUD"],
          link: "https://article-vue.vercel.app/",
          tab: "vue",
        },
        {
          id: 21,
          title: "To-Do List",
          image: "/assets/img/todo.PNG",
          stacks: ["Vue", "Tailwind CSS", "Pinia", "CRUD"],
          link: "https://todolist-vue-aktamov.netlify.app/",
          tab: "vue",
        },
        {
          id: 19,
          title: "TreeView",
          image: "/assets/img/treeview.png",
          stacks: ["Vue", "Tailwind CSS", "Pinia", "CRUD"],
          link: "https://vue-treeview-henna.vercel.app/",
          tab: "vue",
        },
        {
          id: 20,
          title: "Movie List",
          image: "/assets/img/movie.PNG",
          stacks: ["Vue", "Vuex", "CRUD"],
          link: "https://movie-list-psi-six.vercel.app/",
          tab: "vue",
        },
        {
          id: 10,
          title: "Apartments",
          image: "/assets/img/apartments.PNG",
          stacks: ["React", "Context API", "Bootstrap", "Responsive"],
          link: "https://bccreact.vercel.app/",
          tab: "react",
        },
        {
          id: 11,
          title: "Tic Tac Toe (X-0)",
          image: "/assets/img/tic-tac.PNG",
          stacks: ["React", "Context API"],
          link: "https://x-o-game-theta.vercel.app/",
          tab: "react",
        },
        {
          id: 12,
          title: "Max Way",
          image: "/assets/img/max-way.PNG",
          stacks: ["Html", "Css", "Responsive"],
          link: "https://maxway-fastfood.netlify.app/",
          tab: "html",
        },
        {
          id: 6,
          title: "Light Boost e-commerse",
          image: "/assets/img/lightboost.PNG",
          stacks: ["React", "Redux", "Sass", "Bootstrap"],
          link: "https://light-boost-games.vercel.app/",
          tab: "react",
        },
        {
          id: 7,
          title: "E-commerce",
          image: "/assets/img/e-commerce.jpg",
          stacks: ["React", "Context API", "Sass", "Bootstrap", "Responsive"],
          link: "https://ecommerce-website-one.vercel.app/",
          tab: "react",
        },
        {
          id: 13,
          title: "Work Wise",
          image: "/assets/img/workwise.PNG",
          stacks: ["Html", "Css", "Bootstrap"],
          link: "https://workwise.netlify.app/",
          tab: "html",
        },
        {
          id: 16,
          title: "Portfolio Site",
          image: "/assets/img/portfolio.PNG",
          stacks: ["Vue", "Bootstrap"],
          link: "https://aktamovs-dev.vercel.app/",
          tab: "vue",
        },
        {
          id: 8,
          title: "Quiz",
          image: "/assets/img/quiz.PNG",
          stacks: ["Html", "Css", "Javascript", "Responsive"],
          link: "https://quiz-app-two-sandy.vercel.app/",
          tab: "html",
        },
        {
          id: 9,
          title: "Verstka",
          image: "/assets/img/verstka.PNG",
          stacks: ["Html", "Css", "Javascript"],
          link: "https://gilded-douhua-f3574c.netlify.app/",
          tab: "html",
        },
        {
          id: 18,
          title: "Dom-D",

          image: "/assets/img/dom-d.PNG",
          stacks: ["React", "Responsive"],
          link: "https://dom-d-responsive-project-aktamov.netlify.app/",
          tab: "react",
        },
        {
          id: 14,
          title: "Atmosphere",
          image: "/assets/img/Atmosphere.PNG",
          stacks: ["Html", "Css", "Javascript"],
          link: "https://farrux-aktamov-atmosphere-page.netlify.app/",
          tab: "html",
        },
      ],
    };
  },

  methods: {
    selectTab(slug) {
      this.selectedTab = slug;
    },

    filterSites() {
      if (this.selectedTab === "all") {
        return this.sites;
      } else {
        return this.sites.filter((site) => site.tab === this.selectedTab);
      }
    },
  },

  components: {
    Title,
    PortfolioCard,
  },
};
</script>
<style>
</style>