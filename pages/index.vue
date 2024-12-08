<template>
  <div class="home">
    <div class="hero">
      <div class="hero-content">
        <h1 class="gradient-title">✨欢迎使用{{ config.siteName }}</h1>
        <p class="subtitle">基于Cloudflare的个人图床新选择</p>
      </div>
    </div>

    <div class="features">
      <div class="feature-card card">
        <h3>👑 私有化图床</h3>
        <p>注册账户才能上传，有效防止资源滥用</p>
      </div>
      <div class="feature-card card">
        <h3>⚡️ 快速上传</h3>
        <p>支持拖拽上传、粘贴上传图片</p>
      </div>
      <div class="feature-card card">
        <h3>🔒 安全存储</h3>
        <p>数据安全存储，永久保存</p>
      </div>
      <div class="feature-card card">
        <h3>📱 便捷管理</h3>
        <p>在线管理您的所有图片</p>
      </div>
      <div class="feature-card card">
        <h3>💰 极低成本</h3>
        <p>仅需一个域名，其他资源由 Cloudflare 提供</p>
      </div>
      <div class="feature-card card">
        <h3>🤖 TG机器人</h3>
        <p>支持Telegram机器人便捷操作上传</p>
      </div>
      <div class="feature-card card">
        <h3>🎯 智能压缩</h3>
        <p>自动图片压缩技术，节省存储空间</p>
      </div>
      <div class="feature-card card">
        <h3>🎁 更多功能</h3>
        <p>更多实用功能正在开发中，敬请期待</p>
      </div>
    </div>
  </div>
</template>

<script setup>
definePageMeta({
  middleware: 'auth' 
})
const config = useRuntimeConfig()
</script>

<style scoped>
.hero {
  display: flex;
  align-items: flex-start;
  justify-content: space-between;
  max-width: 1200px;
  margin: 0 auto;
  gap: 2rem;
  margin-bottom: 4rem;
}

.hero-content {
  flex: 1;
  text-align: left;

  display: flex;
  flex-direction: column;
  align-items: flex-start;
}

.gradient-title {
  font-size: 2.5rem;
  font-weight: bold;
  background: linear-gradient(45deg, var(--primary-color), #7c3aed);
  -webkit-background-clip: text;
  background-clip: text;
  color: transparent;
  margin-bottom: 1rem;
}

.subtitle {
  font-size: 1.5rem;
  color: var(--text-color-light);
  margin-bottom: 2rem;
}

.action-buttons {
  display: flex;
  gap: 1rem;
}

.btn {
  padding: 0.75rem 1.5rem;
  border-radius: 20px;
  font-weight: 500;
  text-decoration: none;
  display: inline-flex;
  align-items: center;
  gap: 1rem;
}

.btn.primary {
  background: var(--primary-color);
  color: white;
}

.btn.secondary {
  background: var(--card-background);
  color: var(--text-color);
}

.hero-image {
  flex: 1;
  display: flex;
  justify-content: center;
  max-width: 500px;
}

.hero-image img {
  max-width: 100%;
  max-height: 266px;
  width: auto;
  height: auto;
  border-radius: 2rem;
  box-shadow: 0 20px 40px rgba(0, 0, 0, 0.1);
  object-fit: contain;
  filter: drop-shadow(0 0 20px rgba(var(--primary-rgb), 0.4))
         drop-shadow(0 0 40px rgba(var(--primary-rgb), 0.3))
         drop-shadow(0 0 60px rgba(var(--primary-rgb), 0.2));
}

.features {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 2rem;
  margin-top: 2rem;
}

.feature-card {
  padding: 2rem;
  text-align: center;
}

.feature-card h3 {
  margin-bottom: 1rem;
  color: var(--primary-color);
}

@media (max-width: 768px) {
  .hero {
    flex-direction: column;
    text-align: center;
    padding: 0 1rem;
    align-items: center;
  }

  .hero-content {
    text-align: center;
    align-items: center;
    order: 2;
  }

  .gradient-title {
    font-size: 1.5rem;
  }

  .subtitle {
    font-size: 1.2rem;
  }

  .hero-image {
    max-width: 50%;
  }

  .hero-image img {
    max-height: 300px;
  }

  .action-buttons {
    justify-content: center;
  }
}

.github-icon {
  fill: currentColor;
}
</style>
