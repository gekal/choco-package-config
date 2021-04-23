# Chocoコンフィグ

## なぜこれを整理するなの

個人PC用のツールを整理する。

## Chocolatey Install

```powershell
Set-ExecutionPolicy Bypass -Scope Process -Force; iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))
```

## パッケージのインストール

```powershell
# ファイルをダウンロードする。
Invoke-WebRequest -Uri https://raw.githubusercontent.com/gekal/choco-package-config/master/packages.config -OutFile packages.config

# 対象フォルダに移動して、インストールする
# ⇒Long
choco install .\packages.config -y
# ⇒Short
cinst .\packages.config -y
```

## 参照情報

1．[Windowsのパッケージ管理ツール](https://www.gekal.cn/blogs/2018/03/12/windows-package-manager.html)
