<template>
  <div class="right-component">
    <h2>Route</h2>
    <div class="map-container">
      <!-- 地图框 -->
      <div id="map"></div>
    </div>
    <h2>Maintenance List</h2>
    <ul class="maintenance-list">
      <li v-for="item in maintenanceList" :key="item.id">{{ item.name }}</li>
    </ul>
  </div>
</template>

<script>
import L from 'leaflet';
import 'leaflet/dist/leaflet.css';

export default {
  data() {
    return {
      maintenanceList: [
        {id: 1, name: 'Hull Road'},
        {id: 2, name: ' Walmgate pat hole'},
        {id: 3, name: 'xxx'},
        {id: 4, name: 'xxx'}
      ]
    };
  },
  mounted() {
    // 在组件挂载后初始化地图
    this.initMap();
  },
  methods: {
    initMap() {
      // 在此处初始化地图，加载本地地图图像
      const map = L.map('map').setView([51.505, -0.09], 13);
      L.tileLayer('/maps/{z}/{x}/{y}.png', {
        attribution: 'public/maps/map'
      }).addTo(map);
    }
  }
}
</script>

<style scoped>
.right-component {
  background-color: #d0d0d0;
  padding: 10px;
  height: 100%; /* Ensure the component fills its container */
}

h2 {
  text-align: center; /* 居中标题 */
  border: 1px solid black; /* 添加边框 */
  margin-left: 100px;
  margin-right: 100px;
  padding-top: 10px;
  padding-bottom: 10px;
}

.map-container {
  margin-top: 20px;
  height: 200px; /* 设置地图框的高度 */
}

#map {
  width: 100%;
  height: 100%;
}

.maintenance-list {
  margin-top: 80px;
}
.maintenance-list li {
  font-size: 26px; /* 设置字体大小 */
  margin-top: 30px;
}
</style>
