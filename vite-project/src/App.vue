<script setup>
// 这里暂时不需要写复杂的 JS 逻辑
</script>

<template>
  <div class="welcome-container">
    <h1 class="welcome-text">欢迎光临 ✨</h1>
    <p class="subtitle">这是我的第一个 CI/CD 自动化部署项目</p>
    <div class="divider"></div>
  </div>
</template>

<style scoped>
/* 整个容器铺满屏幕并居中对齐 */
.welcome-container {
  height: 100vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  background-color: #242424; /* 高级暗色背景 */
  font-family: 'PingFang SC', 'Microsoft YaHei', sans-serif;
  margin: -8px; /* 抵消默认边距 */
}

/* 欢迎标题：渐变色 + 动画 */
.welcome-text {
  font-size: 5rem;
  font-weight: 800;
  margin: 0;
  /* Vue 经典绿蓝渐变色 */
  background: linear-gradient(135deg, #42d392 0%, #647eff 100%);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  
  /* 添加入场动画 */
  animation: fadeInUp 1.2s ease-out forwards;
}

/* 副标题：延迟出现的动画 */
.subtitle {
  font-size: 1.5rem;
  color: #a0a0a0;
  margin-top: 20px;
  opacity: 0; /* 初始透明 */
  animation: fadeInUp 1.2s ease-out 0.6s forwards; /* 延迟 0.6 秒出现 */
}

/* 装饰性的小线条 */
.divider {
  width: 50px;
  height: 4px;
  background-color: #42d392;
  border-radius: 2px;
  margin-top: 30px;
  opacity: 0;
  animation: scaleIn 1s ease-out 1.2s forwards; /* 延迟 1.2 秒出现 */
}

/* 动画关键帧：从下往上浮现 */
@keyframes fadeInUp {
  from {
    opacity: 0;
    transform: translateY(40px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

/* 动画关键帧：横向展开 */
@keyframes scaleIn {
  from {
    opacity: 0;
    transform: scaleX(0);
  }
  to {
    opacity: 1;
    transform: scaleX(1);
  }
}
</style>