# HTML Tailwind Round Header Table Demo

一个使用HTML和Tailwind CSS实现的表格组件，特点是表头有完整的圆角设计。

## 运行项目

```bash
# 安装依赖
pnpm install

# 启动开发服务器
pnpm start
```

## 技术要点

### 表头圆角实现

本项目使用简单直接的CSS方案实现表头的圆角效果。关键代码：

```css
table {
    border-collapse: collapse;
}

th {
    background-color: rgb(249 250 251);
}

th:first-child {
    border-top-left-radius: 0.75rem;
    border-bottom-left-radius: 0.75rem;
}

th:last-child {
    border-top-right-radius: 0.75rem;
    border-bottom-right-radius: 0.75rem;
}
```

实现原理：
1. 设置表格的`border-collapse: collapse`以消除单元格间的间隙
2. 为所有th设置统一的背景色
3. 给第一个th添加左侧圆角
4. 给最后一个th添加右侧圆角

这种方案的优势：
- 实现简单直接，易于理解和维护
- 不需要使用伪元素和复杂的定位
- 保持了表格的语义化结构
- 代码量少，性能好

## 依赖说明

- Tailwind CSS: 用于样式管理
- Vite: 开发服务器和构建工具
- PostCSS: CSS处理器
- Autoprefixer: 自动添加CSS前缀 