# 🎨 年糕suki - 个人作品集网站

一个充满创意和互动特效的插画师个人作品集网站，展示数字艺术作品的现代化平台。

![Website Preview](https://img.shields.io/badge/Status-Live-brightgreen)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black)

## ✨ 特色功能

### 🎯 视觉效果
- **渐变背景** - 动态紫蓝渐变配色方案
- **粒子动画** - 50个浮动粒子营造梦幻氛围
- **玻璃拟态设计** - 现代化毛玻璃背景模糊效果
- **彩虹文字** - 标题采用渐变色彩效果

### 🚀 交互特效
- **3D悬停效果** - 作品卡片悬停时的立体倾斜动画
- **全屏查看** - 点击作品弹出全屏模态框浏览
- **鼠标跟随** - 鼠标移动时的粒子轨迹特效
- **平滑滚动** - 导航链接的平滑滚动定位

### ⚡ 动画系统
- **页面加载动画** - 渐进式内容显示效果
- **导航动画** - 悬停时的下划线扩展动画
- **卡片动画** - 悬停时的阴影和缩放效果
- **加载器** - 页面初始化时的旋转加载动画

## 🛠️ 技术栈

- **HTML5** - 语义化标记结构
- **CSS3** - 现代CSS特性和动画
- **JavaScript** - 原生JS交互功能
- **Google Fonts** - Poppins字体家族
- **CSS Grid** - 响应式布局系统

## 📁 文件结构

```
portfolio/
├── index.html          # 主页面文件
├── README.md          # 项目说明文档
└── images/            # 作品图片目录
    ├── art1.png
    ├── art2.png
    └── ...
```

## 🚀 快速开始

### 安装和运行

1. **克隆项目**
```bash
git clone https://github.com/yourusername/suki-portfolio.git
cd suki-portfolio
```

2. **添加作品图片**
   - 创建 `images/` 文件夹
   - 将你的作品图片放入该文件夹
   - 推荐尺寸：400x300px 或更高分辨率

3. **修改内容**
   - 在HTML文件中替换占位图片链接
   - 更新作品标题和描述
   - 修改个人信息和联系方式

4. **本地预览**
   - 直接用浏览器打开 `index.html`
   - 或使用本地服务器：
   ```bash
   # 使用Python
   python -m http.server 8000
   
   # 使用Node.js
   npx serve .
   ```

## 🎨 自定义配置

### 更换配色方案
在CSS中修改以下变量：
```css
/* 主渐变色 */
background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);

/* 强调色 */
color: #667eea;
```

### 添加更多作品
在HTML中复制作品卡片结构：
```html
<div class="art" onclick="openModal('art5')">
  <img src="images/your-artwork.jpg" alt="作品5" id="art5" />
  <div class="art-overlay">
    <div class="art-info">
      <h3>作品标题</h3>
      <p>点击查看详情</p>
    </div>
  </div>
  <p>作品名称 5 - 2025</p>
</div>
```

### 调整动画效果
修改动画持续时间和缓动函数：
```css
/* 悬停动画 */
.art:hover {
  transform: translateY(-20px) rotateX(5deg);
  transition: all 0.6s cubic-bezier(0.175, 0.885, 0.32, 1.275);
}
```

## 📱 响应式设计

网站针对不同设备进行了优化：
- **桌面端** (1200px+) - 多列网格布局
- **平板端** (768px-1199px) - 自适应网格
- **手机端** (<768px) - 单列布局，导航调整

## 🌟 核心功能详解

### 粒子系统
```javascript
function createParticles() {
  const particlesContainer = document.getElementById('particles');
  const particleCount = 50; // 可调整粒子数量
  
  for (let i = 0; i < particleCount; i++) {
    // 随机位置和动画延迟
    const particle = document.createElement('div');
    particle.className = 'particle';
    particle.style.left = Math.random() * 100 + '%';
    particle.style.top = Math.random() * 100 + '%';
  }
}
```

### 全屏查看模态框
```javascript
function openModal(imgId) {
  const modal = document.getElementById('imageModal');
  const modalImg = document.getElementById('modalImg');
  const img = document.getElementById(imgId);
  
  modal.style.display = 'block';
  modalImg.src = img.src;
}
```

## 🔧 常见问题

**Q: 如何更换作品图片？**
A: 将图片放在 `images/` 文件夹中，然后在HTML中更新 `src` 属性。

**Q: 如何修改联系信息？**
A: 在 `#contact` 部分更新邮箱和社交媒体链接。

**Q: 动画太快/太慢怎么办？**
A: 在CSS中调整 `transition` 和 `animation-duration` 属性。

**Q: 如何添加新的页面部分？**
A: 复制现有的 `<section>` 结构，并在导航中添加对应链接。

## 📈 性能优化

- 使用 CSS3 硬件加速动画
- 图片懒加载（可选扩展）
- 最小化重排和重绘
- 优化CSS选择器性能

## 🎯 浏览器支持

- Chrome 60+
- Firefox 55+
- Safari 12+
- Edge 79+

## 📄 许可证

MIT License - 可自由使用和修改

## 👨‍💻 作者

**年糕suki** - 插画师 | 数字艺术家 | 美术生

- 邮箱: F.W@example.com
- 米画师: [查看作品](https://www.mihuashi.com/profiles/522429)
- 画加: [查看作品](https://huajia.163.com/main/profile/LBpjp17r)

---

💖 **如果这个项目对你有帮助，请给个 Star！**

🚀 **持续更新中，欢迎提交 Issue 和 PR！**
