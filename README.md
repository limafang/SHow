# SHow 实验数据管理面板

本项目由 claude 编写

一个用于管理和比较实验数据的网页应用，支持创建、编辑、比较和导出实验数据。

## 功能特点

### 数据管理
- ✨ 创建新的实验记录
- 📝 编辑现有实验数据
- 🗑️ 支持单个和批量删除
- 💾 自动保存到本地存储
- 📤 导出选中的实验数据为CSV格式

### 实验内容
- 📋 记录实验名称和参数
- 💭 记录LLM思考过程
- 📊 保存实验结果
- 🏷️ 自动根据参数生成标签

### 数据展示
- 🔍 展开/收起思考过程和结果
- 🔄 保持内容展开状态
- 📊 多实验对比视图
- 🏷️ 基于标签筛选实验

### 用户体验
- 💡 直观的卡片式布局
- ✅ 清晰的选择状态指示
- 🎯 便捷的批量操作
- 📱 响应式设计

## 使用说明

### 创建实验
1. 点击右上角的"创建实验卡片"按钮
2. 填写实验信息：
   - 实验名称
   - 实验参数（每行一个，将自动作为标签）
   - Prompt内容
   - LLM思考过程
   - 实验结果
3. 点击"创建"保存实验

### 查看和编辑
- 点击卡片上的"思考过程"或"查看结果"可展开对应内容
- 选中单个卡片后可以点击"编辑"按钮修改内容
- 展开的内容在选择或取消选择卡片时会保持状态

### 批量操作
1. 点击卡片选择多个实验
2. 使用顶部工具栏的按钮进行操作：
   - "删除所选"：删除选中的实验
   - "比对选中卡片"：打开对比视图
   - "导出数据"：导出选中实验的CSV文件

### 标签筛选
1. 点击"选择标签筛选"按钮
2. 选择需要的标签
3. 实验列表将自动更新显示匹配的实验

## 技术实现

### 前端技术
- 原生JavaScript
- HTML5
- CSS3 (Flexbox, Grid, Transitions)

### 数据存储
- 使用浏览器的localStorage实现数据持久化
- 自动保存所有操作

### 性能优化
- 使用事件委托处理交互
- 优化DOM操作，避免不必要的重渲染
- 异步处理数据导出

## 浏览器支持
- Chrome (推荐)
- Firefox
- Safari
- Edge

## 开发说明
项目使用纯前端技术栈，无需构建工具和后端服务器。直接在浏览器中打开 `experiment-dashboard.html` 即可使用。

### 本地开发
1. 克隆项目到本地
2. 使用浏览器打开 `experiment-dashboard.html`
3. 所有数据将保存在浏览器的localStorage中

## 注意事项
- 使用localStorage存储数据，请定期导出重要数据
- 清除浏览器数据可能会导致保存的实验数据丢失
- 建议定期使用导出功能备份数据