# ppt-style-transfer

## 包来源与状态

- 类型：用户已安装 Skill 的完整收录包，包含 `SKILL.md`、`agents/openai.yaml` 和两个 `references/` 文档。
- 来源：用户提供并授权收录、公开发布的 `ppt-style-transfer` 包；公开仓库为 [ppt-style-transfer](https://github.com/zylallenarcher-beep/ppt-style-transfer)。
- 本包记录完整工作流，不依据目录快照推断实际调用、成稿制作、测试通过或发布使用情况。
- 未捆绑第三方代码、字体、图片或其他素材；当前包未指定许可证。

## 范围与触发

用于已有 PPT 按参考演示稿、页面截图或已确认风格进行视觉改版、重排、样张制作和成稿核验。支持固定结构与页数、明确授权后重排增页、先提增页数量方案三种模式。

保真范围、可编辑程度、输出类型和结构权限以当次要求为准。单纯数字更新、从零写稿和业务事实审计不属于默认范围。

## 能力与边界

提取视觉规则、建立来源内容映射、核对数字上下文、检查最终文件内容，并通过实际渲染检查缺字、裁切、重叠与换行。整页图片和合成背景中的元素不能声明为全部可编辑；没有实际渲染条件时需说明未验证部分。

## 依赖与安装

依赖宿主环境提供演示文件读取、制作、导出和渲染能力。本包不自带运行时或服务。`pptx`、`baoyu-design`、`imagegen` 是按路线选用的集成名称，未随本包分发，可由同等能力工具替代；HTML、图片生成与 Windows PowerPoint COM 均按实际需要使用。

将完整目录安装为 `~/.codex/skills/ppt-style-transfer`；自定义 `CODEX_HOME` 时使用其 `skills/ppt-style-transfer`。用法见 [README.md](README.md)，执行规则见 [SKILL.md](SKILL.md)。
