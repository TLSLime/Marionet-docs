# GitHub Pages 部署快速修复指南

## 问题诊断

您遇到的错误：`Failed to create deployment (status: 404)` 通常表示 GitHub Pages 没有正确启用。

## 解决步骤

### 1. 启用 GitHub Pages

1. 访问：https://github.com/TLSLime/Marionet-docs/settings/pages
2. 在 "Source" 部分选择 "GitHub Actions"
3. 点击 "Save"

### 2. 如果看不到 "GitHub Actions" 选项

请检查：
- [ ] 仓库是公开的（Public）
- [ ] 您有管理员权限
- [ ] 仓库中存在 `.github/workflows/docs.yml` 文件

### 3. 重新触发部署

方法一：推送新提交
```bash
git add .
git commit -m "修复GitHub Pages部署"
git push origin main
```

方法二：手动重新运行
1. 进入 Actions 页面
2. 找到 "部署文档到 GitHub Pages" 工作流
3. 点击 "Re-run all jobs"

### 4. 验证部署

部署成功后，访问：
https://tlslim.github.io/Marionet-docs/

## 常见问题

**Q: 为什么会出现404错误？**
A: 通常是因为 GitHub Pages 没有启用，或者仓库权限设置不正确。

**Q: 需要等待多长时间？**
A: 通常需要2-5分钟，有时可能需要更长时间。

**Q: 如何确认部署成功？**
A: 在 Actions 页面查看工作流状态，显示绿色勾号表示成功。

## 联系支持

如果问题仍然存在，请：
1. 检查 [GitHub Pages 文档](https://docs.github.com/en/pages)
2. 在项目 Issues 中报告问题
3. 提供完整的错误日志
