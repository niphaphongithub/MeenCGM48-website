<template>
  <div class="popup-overlay">
    <div class="popup-content">
      <div class="popup-scroll">
        <slot></slot>
      </div>
      <button class="close-button" @click="$emit('close')">&times;</button>
    </div>
  </div>
</template>
  
  <script>
export default {
  name: "PopupSCMeen",
};
</script>
  
  <style scoped>
.popup-overlay {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.5);
  display: flex;
  justify-content: center;
  align-items: center;
}

.popup-content {
  background-color: #fff;
  padding: 16px;
  border-radius: 4px;
  text-align: center;
  position: relative;
  max-width: 80%;
  max-height: 80%;
  overflow: auto;
}

.close-button {
  position: absolute;
  top: 8px;
  right: 8px;
  background: none;
  border: none;
  font-size: 20px;
  color: #000;
  cursor: pointer;
}

/* Custom styles */
.popup-content {
  background-color: #f9f9f9;
  padding: 20px;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.15);
}

.close-button {
  font-size: 24px;
  color: #aaa;
  transition: color 0.3s;
}

.close-button:hover {
  color: #777;
}

.popup-content img {
  width: 500px;
  margin-bottom: 16px;
}
::-webkit-scrollbar {
  width: 8px;
}

::-webkit-scrollbar-thumb {
  background-color: #C2CDFF;
  border-radius: 1px;
}

::-webkit-scrollbar-thumb:hover {
  background-color: #555;
}

::-webkit-scrollbar-track {
  background-color: #f1f1f1;
  border-radius: 1px;
}
</style>
  