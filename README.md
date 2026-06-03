# create-ip-travel-postcards

一个用于 Codex 的文旅明信片生成 skill：把用户提供的 IP 角色与指定景点、月份结合，生成统一系列感的正面 + 反面 3:2 横版明信片。

## 适合做什么

- IP 角色结合旅行地、景点、季节，生成文旅明信片
- 先生成一套正反面样板，确认后再作为系列锚点批量扩展
- 正面偏植物标本插画 + 景点叙事
- 反面偏复古明信片排版，包含诗句、邮票、地址线和印章
- 绘图目标模型为 GPT Image 2

## 安装链接

真正的 skill 位于仓库中的这个目录：

```text
skills/create-ip-travel-postcards/
```

如果你的平台支持“从 GitHub 链接安装 skill”，请使用这个链接：

```text
https://github.com/dorlarosendo434-hub/create-ip-travel-postcards/tree/main/skills/create-ip-travel-postcards
```

这个链接已经指向具体 skill 目录，安装器可以从链接中解析路径。

## Codex 脚本安装

在 Codex 中，可以用官方安装脚本直接安装上面的 GitHub 链接：

```powershell
python -X utf8 "$env:USERPROFILE\.codex\skills\.system\skill-installer\scripts\install-skill-from-github.py" `
  --url "https://github.com/dorlarosendo434-hub/create-ip-travel-postcards/tree/main/skills/create-ip-travel-postcards"
```

安装完成后，重启 Codex 让新 skill 生效。

## 使用方式

在 Codex 中可以这样调用：

```text
使用 $create-ip-travel-postcards，为我的 IP 生成一套景点文旅明信片。
```

## 需要提供的信息

必填：

- IP 角色参考图
- 景点名称 + 所在地
- 推荐月份
- 景点关键词 2-5 个

可选：

- IP 昵称
- 四行诗歌
- 已确认的同系列正面图或反面图，用于风格对齐

## 打包文件

仓库内也保留了一个可分发 ZIP：

```text
dist/create-ip-travel-postcards.zip
```

日常通过 GitHub 链接安装时不需要使用这个 ZIP。

