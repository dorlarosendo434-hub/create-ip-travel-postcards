# create-ip-travel-postcards

文旅明信片生成 skill：把用户提供的 IP 角色与指定景点、月份结合，生成统一系列感的正面 + 反面 3:2 横版明信片。

## 分享链接

直接分享这个仓库链接即可：

```text
https://github.com/dorlarosendo434-hub/create-ip-travel-postcards
```

本仓库根目录就是 skill，核心文件直接位于根目录：

```text
SKILL.md
agents/
assets/
references/
```

## Codex 安装

如果使用 Codex 官方安装脚本，可以这样安装：

```powershell
python -X utf8 "$env:USERPROFILE\.codex\skills\.system\skill-installer\scripts\install-skill-from-github.py" `
  --repo dorlarosendo434-hub/create-ip-travel-postcards `
  --path . `
  --name create-ip-travel-postcards
```

安装后重启 Codex。

## 使用方式

```text
使用 $create-ip-travel-postcards，为我的 IP 生成一套景点文旅明信片。
```

必填信息：

- IP 角色参考图
- 景点名称 + 所在地
- 推荐月份
- 景点关键词 2-5 个

可选信息：

- IP 昵称
- 四行诗歌
- 已确认的同系列正面图或反面图

## 打包文件

```text
dist/create-ip-travel-postcards.zip
```

