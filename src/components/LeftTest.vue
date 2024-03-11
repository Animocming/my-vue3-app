<template>
  <div class="photo-component">
<!--    <h2>Photo Component</h2>-->
    <div class="photo-list">
      <img src="@/assets/img1.png" alt="Photo 1" @click="handlePhotoClick(1)" />
      <img src="@/assets/img2.png" alt="Photo 2" @click="handlePhotoClick(2)" />
      <img src="@/assets/img3.png" alt="Photo 3" @click="handlePhotoClick(3)" />
    </div>
  </div>
</template>

<script>
export default {
  methods: {
    handlePhotoClick(index) {
      alert(`Clicked on photo ${index}`);
      // 在这里执行您希望的点击事件处理逻辑
    }
  }
}
</script>

<style scoped>
.photo-component {
  background-color: #d0d0d0;
  padding: 10px;
  height: 100%; /* Ensure the component fills its container */
}

.photo-list {
  margin-top: 20px;
  display: flex;
  flex-direction: column;
}

.photo-list img {
  display: block;
  margin-bottom: 10px;
  cursor: pointer;
}

</style>
