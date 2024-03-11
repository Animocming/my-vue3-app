<template>
  <div class="photo-component" style="overflow: hidden; position: relative;">
<!--    <h2>Photo Component</h2>-->
    <div class="photo-list">
      <img src="@/assets/camera1.png" alt="Photo 1" @click="handlePhotoClick(1)" style="width: 50%; height: auto; margin-top: 20px;" />
      <img src="@/assets/gallery1.png" alt="Photo 2" @click="handlePhotoClick(2)" style="width: 50%; height: auto; margin-top: 20px;" />
      <img src="@/assets/streamcamera.png" alt="Photo 3" @click="handlePhotoClick(3)" style="width: 50%; height: auto; margin-top: 20px;" />
    </div>
    <img src="@/assets/profile.png" alt="Photo 4" style="position: absolute; bottom: 30px; left: 50%; transform: translateX(-50%); width: 50%; height: auto; margin-bottom: 70px;" />
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
  position: relative; /* 设置相对定位以便子元素可以使用绝对定位 */
}

.photo-list {
  margin-top: 120px;
  display: flex;
  flex-direction: column;
  align-items: center; /* 在垂直方向上居中 */
}

.photo-list img {
  display: block;
  margin-bottom: 50px;
  cursor: pointer;
  //border: black  solid 2px;
}
</style>
