<template>
  <div class="card-container">
    <div class="card">
      <div class="image-container">
        <img :src="imageSrc" alt="Card Image" />
      </div>
      <div class="align-left-card">
        <div class="content">
          <h2>𝐂𝐆𝐌𝟒𝟖 𝟔𝐭𝐡 𝐒𝐢𝐧𝐠𝐥𝐞</h2>
          <p>
            "𝑺𝒂𝒏𝒔𝒆𝒊 𝑲𝒂𝒘𝒂𝒊𝒊! - เธออะ 𝑲𝒂𝒘𝒂𝒊𝒊!"<br />
            🤝 Handshake Event 🤝<br />
            [ #จับมือเธอแล้วมันKawaii ]
          </p>
          <slot></slot>
          <div class="button-container">
            <button class="custom-button" @click="openPopup">
              See More Details
            </button>
          </div>
          <Popup v-if="isPopupOpen" @close="closePopup">
            <h2>𝐂𝐆𝐌𝟒𝟖 𝟔𝐭𝐡 𝐒𝐢𝐧𝐠𝐥𝐞</h2>
          <p>
            "𝑺𝒂𝒏𝒔𝒆𝒊 𝑲𝒂𝒘𝒂𝒊𝒊! - เธออะ 𝑲𝒂𝒘𝒂𝒊𝒊!"<br />
            🤝 Handshake Event 🤝<br />
            [ #จับมือเธอแล้วมันKawaii ]
          </p>
            <img :src="imageSrc" alt="Popup Image 1" />
          </Popup>
        </div>
      </div>
    </div>
  </div>
</template>
  
  <script>
import Popup from "./Popup.vue";
export default {
  name: "CardSCMeeen",
  components: {
    Popup,
  },
  props: {
    title: {
      type: String,
      required: true
    },
    description: {
      type: String,
      required: true
    },

    imageSrc: {
      type: String,
      required: true,
    },
  },

  data() {
    return {
      isPopupOpen: false,
    };
  },
  methods: {
    openPopup() {
      this.isPopupOpen = true;
    },
    closePopup() {
      this.isPopupOpen = false;
    },
  },
};
</script>
  
  <style scoped>
.card-container {
  display: grid;
  justify-content: center;
  align-items: center;
  /* height: 100vh; */
}
.card {
  display: flex;
  align-items: center;
  border: 1px solid #ccc;
  border-radius: 4px;
  padding: 16px;
  margin: 20px;
  width: 600px;
}

.image-container {
  flex: 0 0 auto;
  margin-right: 16px;
}

.image-container img {
  width: 300px;
  height: auto;
}

.content {
  display: flex;
  flex-direction: column;
  align-items: center;
}

.button-container {
  margin-top: 8px;
}

.align-left-card {
  width: 100%;
  height: 100%;
}

p {
  margin-top: 8px;
  text-align: center;
}

.custom-button {
  padding: 8px 16px;
  background-color: #6d88ff;
  color: #fff;
  border: none;
  border-radius: 4px;
  cursor: pointer;
  font-size: 14px;
  transition: background-color 0.3s;
}

.custom-button:hover {
  background-color: #a2c7ff;
}

img {
    width: 700px;
    margin-bottom: 16px;
  }

@media (max-width: 768px) {
  .card {
    padding: 8px;
    width: 350px;
    margin-left: 5px;
    margin-right: 5px;
  }

  .image-container img {
    width: 150px;
  }
}
</style>
  