把下面的复制到 memos 的 style 输入栏保存即可 下面有内容展示
```bash

/* 全局基础样式 */
html, body {
    margin: 0;
    padding: 0;
    width: 100%;
    min-height: 100vh;
    overflow: auto;
    background-color: rgba(244, 244, 245, 0);
    font-size: 1rem;
}
/* 使用更高优先级的选择器来确保颜色样式生效 */
/*标签的颜色*/
body .text-blue-600 {
    color: rgb(254 254 254) !important;
}
/*右边标签的颜色*/
body .text-gray-600 {
    color: rgb(223 233 133) !important;
}
/*时间标签的颜色*/
body .text-gray-400 {
    color: rgb(2 344 1334) !important;
}
/*附带文件标签的颜色*/
body .text-gray-500{
    color: rgb(124 233333 23) !important;
}
/*内容文本的颜色*/
body .text-gray-800 {
    color: rgb(63 206 83) !important;
}

/* 视频背景容器 */
.video-background {
    position: fixed;
    inset: 0; /* 替代 top:0; left:0; width:100%; height:100% */
    overflow: hidden;
    z-index: -1;
}

#background-video {
    width: 100%;
    height: 100%;
    object-fit: cover;
}

/* Memos 标签样式 */
.memo-tag {
    display: inline-block;
    color: #f3f3f3;
    padding: 2px 6px;
    font-size: 15px;
    margin-bottom: 4px;
    border-radius: 2px;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
}

/* 不同标签的背景色 */
.memo-tag:nth-child(1) { background-color: #40b76b; }
.memo-tag:nth-child(2) { background-color: #5febe0; }
.memo-tag:nth-child(3) { background-color: #f298a6; }
.memo-tag:nth-child(4) { background-color: #fdb15d; }
.memo-tag:nth-child(5) { background-color: #67d6ca; }
.memo-tag:nth-child(6) { background-color: #ad96fe; }

/* 高亮文本 */
mark {
    background-color: #F27579;
    color: #f3f3f3;
    padding: 0 2px;
    border-radius: 2px;
}

/* 背景模糊效果 */
.blur-bg {
    background-color: rgba(255, 255, 255, 0.66);
    backdrop-filter: blur(20px);
}

/* 特定元素的模糊效果 */
.w-full.bg-zinc-100,
.bg-white,
.hover\:bg-white:hover,
.memo-wrapper,
.bg-gray-200,
.memo-editor-container {
    @extend .blur-bg;
}

.bg-zinc-50 {
    background-color: rgba(250, 250, 250, 0.66);
    backdrop-filter: blur(20px);
}

/* Dark 模式调整 */
.dark {
    & .dark\:bg-zinc-700,
    & .dark\:hover\:bg-zinc-700:hover {
        @extend .blur-bg;
    }

    & .dark\:bg-zinc-800,
    & header.dark\:bg-zinc-800,
    & aside.dark\:bg-zinc-800 {
        background-color: transparent;
    }

    & .dark\:bg-zinc-900 {
        background-color: rgba(24, 24, 27, 1);
    }

    & .dark\:bg-opacity-40 {
        background-color: rgba(0, 0, 0, 0.4);
        backdrop-filter: blur(20px);
    }

    & .dark\:border-zinc-800 {
        border-color: rgba(39, 39, 42, 1);
        backdrop-filter: blur(20px);
    }
}

/* 文章背景 */
.bg-white {
    background-color: rgba(231, 228, 228, 0.2);
    backdrop-filter: blur(20px);
}

/* 隐藏关于链接 */
#header-about {
    display: none;
}

/* 悬浮按钮 */
#chat-button {
    position: fixed;
    bottom: 20px;
    right: 20px;
    width: 50px;
    height: 50px;
    background-color: #007bff;
    color: white;
    border: none;
    border-radius: 50%;
    font-size: 24px;
    display: flex;
    align-items: center;
    justify-content: center;
    cursor: pointer;
    z-index: 1000;
}

/* 对话框 */
#chat-popup {
    display: none;
    position: fixed;
    bottom: 80px;
    right: 20px;
    width: 300px;
    height: 400px;
    background: white;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
    border-radius: 8px;
    overflow: hidden;
    z-index: 1000;
}

#chat-popup iframe {
    width: 100%;
    height: 100%;
    border: none;
}
```

