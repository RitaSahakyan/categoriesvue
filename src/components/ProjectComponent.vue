<template>
    <div class="project-card" :class="size">
      <img :src="imageSrc" alt="Изображение проекта" />
      <div class="info">
        <div class="info-text">
            <h3 class="title">{{ title }}</h3>
            <p class="description">{{ description }}</p>
        </div>
        <button class="action-button">
          <img :src="require(`@/assets/${buttonIcon}`)" alt="Иконка кнопки" />
        </button>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    props: {
      imageSrc: {
        type: String,
        required: true
      },
      size: {
        type: String,
        default: "large",
        validator: (value) => ["large", "small"].includes(value)
      },
      title: {
        type: String,
        required: true
      },
      description: {
        type: String,
        required: true
      },
      buttonIcon: {
        type: String,
        required: true
      }
    }
  };
  </script>
  
  <style scoped>
  .project-card {
    width: 585px;
    display: flex;
    flex-direction: column;
    overflow: hidden;
    margin-bottom: 24px;
  }
  
  .project-card img {
    width: 100%;
    object-fit: cover;
  }
  
  .project-card.large {
    height: 947px;
  }
  
  .project-card.small {
    height: 616px;
  }
  
  .info {
    display: flex;
    justify-content: space-between;
    height: 100%;
    padding: 16px;
  }
  
  .title {
    font-size: 25px;
    margin: 0;
  }
  
  .description {
    font-size: 22px;
    margin: 0;
  }
  
  .action-button {
    width: 52px;
            height: 52px;
            background-color: #F4F0EC;
            border-radius: 50%;
            border: none;
  }
  
  .action-button img {
    width: 30px;
  }
  </style>
  