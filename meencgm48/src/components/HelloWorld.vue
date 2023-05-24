<template>
  <div class="slideshow">
    <img :src="currentImage" :alt="currentImageAlt" class="slide">
  </div>
</template>

<script>
export default {
  data() {
    return {
      images: [
        { url: 'https://scontent.fbkk13-1.fna.fbcdn.net/v/t39.30808-6/344535427_249402907582335_5054365874551369427_n.jpg?_nc_cat=108&ccb=1-7&_nc_sid=730e14&_nc_eui2=AeERqIJasqXWdPeJr7KqvDAPpi3UVtLx7XqmLdRW0vHteop29fVa5Dut6AAfF7hpjU_Sn2XR_g0fSiYDYESASR7Q&_nc_ohc=WO6226bbaHwAX-6SsWs&_nc_ht=scontent.fbkk13-1.fna&oh=00_AfBflaMNEilHh84hKIof1IPE0USQ1jsCbPwLksHlztupJQ&oe=6471E979', alt: 'Image 1' },
        { url: 'https://scontent.fbkk13-1.fna.fbcdn.net/v/t39.30808-6/344559966_778983850521282_3494119763069063421_n.jpg?_nc_cat=108&ccb=1-7&_nc_sid=730e14&_nc_eui2=AeFf6SSjGm6ltg16iRuBpxE6azUjReKUayBrNSNF4pRrINWVfDLndWl9PvkJ_5gFNBtJraKl4Bv9Hh7O7-bekYla&_nc_ohc=iFihFYfM6WMAX9DY6vi&_nc_ht=scontent.fbkk13-1.fna&oh=00_AfBBwQh8gJcqiTaceSW0z-EPwpvRG_IybRQdutIHZZqAGg&oe=6472CF0D', alt: 'Image 2' },
        { url: 'https://scontent.fbkk13-3.fna.fbcdn.net/v/t39.30808-6/344572491_624485319541274_5417063493663797018_n.jpg?_nc_cat=110&ccb=1-7&_nc_sid=730e14&_nc_eui2=AeE0zv8pb_gfuNpUBhzIp7MdIJ0a9X_heG8gnRr1f-F4b44sU2IxNLijNC4loNn_Uo7uyR-HQw3QSpPp2bpq4u8y&_nc_ohc=dA8UyOb2CaMAX8nwn1b&_nc_ht=scontent.fbkk13-3.fna&oh=00_AfCuEPgnJxnngOwg4Q_MoJMSUIykSd9rs03nKl2w37lHXg&oe=647336DC', alt: 'Image 3' }
      ],
      currentImageIndex: 0
    };
  },
  mounted() {
    this.startSlideshow();
  },
  methods: {
    startSlideshow() {
      setInterval(() => {
        this.currentImageIndex = (this.currentImageIndex + 1) % this.images.length;
      }, 3000); // เปลี่ยนภาพทุก 3 วินาที
    }
  },
  computed: {
    currentImage() {
      return this.images[this.currentImageIndex].url;
    },
    currentImageAlt() {
      return this.images[this.currentImageIndex].alt;
    }
  }
};
</script>

<style>
.slideshow {
  width: 100%;
  height: 980px;
  position: relative;
  overflow: hidden;
}

.slide {
  width: 100%;
  height: 100%;
  object-fit: cover;
  transition: opacity 0.5s ease;
}

</style>

  