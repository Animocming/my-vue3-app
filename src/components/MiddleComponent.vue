<template>
  <div class="middle-component">
    <h2 style="font-size: 40px">York Sport Village</h2>
    <table class="images-table">
      <!-- 标题行 -->
      <tr>
        <td><h2>Video/Picture feed</h2></td>
        <td><h2>Detection Outcome</h2></td>
      </tr>
      <!-- 图片行 -->
      <tr>
        <td class="image-container">
          <img src="../assets/00666-1.jpg" alt="图片1" class="image">
        </td>
        <td class="image-container">
          <img src="../assets/00666-2.jpg" alt="图片2" class="image">
        </td>
      </tr>
    </table>
    <!-- 按钮容器 -->
    <div class="buttons-container">
      <button>Correct</button>
      <button>Incorrect</button>
    </div>

  </div>
</template>

<script>
export default {
  name: 'MiddleComponent',
};
</script>

<style scoped>
.middle-component {
  background-color: #e0e0e0;
  padding: 10px;
  position: relative;
  height: auto;
  display: flex;
  flex-direction: column;
  align-items: center;
}

.images-table {
  margin-top: 0;
  width: 100%;
  border-collapse: collapse;
}

.image-container, td {
  text-align: center;
  padding: 10px;
}

.image {
  width: 750px; /* 设置固定宽度 */
  height: auto;
}


.buttons-container {
  position: absolute;
  right: 110px;
  bottom: 10px;
  margin-bottom: 290px;
}

button {
  padding: 25px 60px;
  margin: 0 5px;
  font-size: 30px;
  cursor: pointer;
  font-weight: bold;
}

</style>
