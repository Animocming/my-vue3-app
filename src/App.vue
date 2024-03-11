<template>
  <div class="container">
     <left-component class="left"></left-component>
<!--    <LeftTest class="left"></LeftTest>-->
    <middle-component class="middle"></middle-component>
    <right-component class="right"></right-component>

  </div>
</template>

<script>
import LeftComponent from './components/LeftComponent.vue';
import MiddleComponent from './components/MiddleComponent.vue';
import RightComponent from './components/RightComponent.vue';

// import LeftTest from "@/components/LeftTest.vue";

export default {
  name: 'App',
  components: {
    LeftComponent,
    MiddleComponent,
    RightComponent
    // LeftTest
  },
  mounted() {
    // 隐藏滚动条
    document.body.style.overflow = 'hidden';
    document.documentElement.style.overflow = 'hidden';
  },
  beforeUnmount() {
    // 恢复滚动条
    document.body.style.overflow = '';
    document.documentElement.style.overflow = '';
  }
}
</script>

<style>
.container {
  display: flex;
  flex-direction: row;
  height: 100vh; /* 设置容器高度为视口高度 */
}

.right {
  flex: 6;
}

.left {
  flex: 2;
}

.middle {
  flex: 16;
}

/* 样式可以根据你的需求进行调整 */
</style>
<!--&#45;&#45;&#45;&#45;&#45;&#45;&#45;&#45;&#45;&#45;&#45;&#45;&#45;&#45;&#45;&#45;&#45;&#45;&#45;&#45;&#45;&#45;&#45;&#45;&#45;&#45;&#45;&#45;&#45;&#45;&#45;&#45;&#45;&#45;&#45;&#45;&#45;&#45;-->

