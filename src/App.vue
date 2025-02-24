<template>
  <div id="app">
    <AppHeader />
    <HeaderComponent />
    <div class="container">
      <CategoriesComponent @category-selected="changeCategory" />
      <div class="gallery">
        <ProjectComponent 
          v-for="(image, index) in filteredImages" 
          :key="index" 
          :imageSrc="image.src" 
          :size="image.size" 
          :title="image.title" 
          :description="image.description"
          :buttonIcon="image.buttonIcon" 
        />
      </div>
      <PaginationComponent />
    </div>
    <AppFooter />
  </div>
</template>

<script>
import AppFooter from './components/AppFooter.vue';
import AppHeader from './components/AppHeader.vue';
import CategoriesComponent from './components/CategoriesComponent.vue';
import HeaderComponent from './components/HeaderComponent.vue';
import PaginationComponent from './components/PaginationComponent.vue';
import ProjectComponent from './components/ProjectComponent.vue';
PaginationComponent

export default {
  name: 'App',
  components: {
    AppHeader,
    HeaderComponent,
    CategoriesComponent,
    ProjectComponent,
    PaginationComponent,
    AppFooter,
  },
  data() {
    return {
      currentCategory: 'Спальня',
      imagesData: {
        'Спальня': [
        {
          src: require('@/assets/Proj1.svg'),
          size: "large",
          title: "Минималистичная спальня",
          description: "Декор / Планировка",
          buttonIcon: "arrow.png"
        },
        {
          src: require('@/assets/Proj2.svg'),
          size: "small",
          title: "Минималистичная спальня",
          description: "Декор / Планировка",
          buttonIcon: "arrow.png"
                },
        {
          src: require('@/assets/Proj3.svg'),
          size: "small",
          title: "Классическая спальня",
          description: "Декор / Планировка",
          buttonIcon: "arrow.png"
                },
        {
          src: require('@/assets/Proj4.svg'),
          size: "small",
          title: "Современная спальня",
          description: "Декор / Планировка",
          buttonIcon: "arrow.png"
                },
        {
          src: require('@/assets/Proj5.svg'),
          size: "large",
          title: "Минималистичный прикроватный столик",
          description: "Декор / Планировка",
          buttonIcon: "arrow.png"
                },
        {
          src: require('@/assets/Proj6.svg'),
          size: "small",
          title: "Столы и столики",
          description: "Декор / Планировка",
          buttonIcon: "arrow.png"
                },
        {
          src: require('@/assets/Proj7.svg'),
          size: "small",
          title: "Современная спальня",
          description: "Декор / Планировка",
          buttonIcon: "arrow.png"
                },
        {
          src: require('@/assets/Proj8.svg'),
          size: "small",
          title: "Современная спальня",
          description: "Декор / Планировка",
          buttonIcon: "arrow.png"
                }
                ],
        'Ванная комната': [
          {
            src: require('@/assets/bath1.jpg'),
            size: "large",
            title: "Современная ванная",
            description: "Декор / Планировка",
            buttonIcon: "arrow.png"
          },
          {
            src: require('@/assets/bath3.jpg'),
            size: "large",
            title: "Минималистичная ванная",
            description: "Декор / Планировка",
            buttonIcon: "arrow.png"
          }
          
        ],
        'Кухня': [
          {
            src: require('@/assets/kitchen1.jpg'),
            size: "large",
            title: "Современная кухня",
            description: "Декор / Планировка",
            buttonIcon: "arrow.png"
          },
          {
            src: require('@/assets/kitchen3.jpeg'),
            size: "large",
            title: "Современная кухня",
            description: "Декор / Планировка",
            buttonIcon: "arrow.png"
          }
        ],
        'Гостиная': [
          {
            src: require('@/assets/living1.jpg'),
            size: "large",
            title: "Классическая гостиная",
            description: "Декор / Планировка",
            buttonIcon: "arrow.png"
          },
          {
            src: require('@/assets/living2.jpeg'),
            size: "small",
            title: "Современная гостиная",
            description: "Декор / Планировка",
            buttonIcon: "arrow.png"
          },
          {
            src: require('@/assets/living3.jpg'),
            size: "large",
            title: "Классическая гостиная",
            description: "Декор / Планировка",
            buttonIcon: "arrow.png"
          },
          {
            src: require('@/assets/living4.jpg'),
            size: "large",
            title: "Современная гостиная",
            description: "Декор / Планировка",
            buttonIcon: "arrow.png"
          }
        ]
      }
    };
  },
  computed: {
    filteredImages() {
      return this.imagesData[this.currentCategory] || [];
    }
  },
  methods: {
    changeCategory(category) {
      this.currentCategory = category;
    }
  }
};
</script>


<style scoped>
.gallery {
  display: flex;
  flex-wrap: wrap;
  gap: 20px;
}
</style>
