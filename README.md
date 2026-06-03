# create-ip-travel-postcards

一个用于 Codex 的文旅明信片生成 skill：把用户提供的 IP 角色与指定景点、月份结合，生成统一系列感的正面 + 反面 3:2 横版明信片。

## 适合做什么

- IP 角色结合旅行地、景点、季节，生成文旅明信片
- 先生成一套正反面样板，确认后再作为系列锚点批量扩展
- 正面偏植物标本插画 + 景点叙事
- 反面偏复古明信片排版，包含诗句、邮票、地址线和印章
- 绘图目标模型为 GPT Image 2

## 推荐安装方式

这个仓库已经调整为“仓库根目录就是 skill”，根目录直接包含：

```text
SKILL.md
agents/
assets/
references/
```

如果你的平台支持通过 GitHub 仓库链接安装根目录 skill，直接使用这个链接即可：

```text
https://github.com/dorlarosendo434-hub/create-ip-travel-postcards
```

## Codex 脚本安装

Codex 当前的官方安装脚本仍然需要显式指定路径。因为本仓库根目录就是 skill，所以路径使用 `.`，并用 `--name` 指定安装后的 skill 名称：

```powershell
python -X utf8 "$env:USERPROFILE\.codex\skills\.system\skill-installer\scripts\install-skill-from-github.py" `
  --repo dorlarosendo434-hub/create-ip-travel-postcards `
  --path . `
  --name create-ip-travel-postcards
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

日常通过 GitHub 安装时不需要使用这个 ZIP。

