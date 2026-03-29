# dotfilesの整理は仕事術の整理！生産性向上まったなし！

<!-- https://findy.connpass.com/event/387107/ -->

Atusy

## ![height:1em](images/headphone.jpg) atusy

- Engineering Manager兼Dev
- 好きなもの
    - Neovim
    - コーヒー（焙煎からやる）
- 著書にRが生産性を高める 〜データ分析ワークフロー効率化の実践

![](https://gihyo.jp/assets/images/cover/2022/9784297125240.jpg)

## フォローよろしく！

* <https://github.com/atusy>
* <https://x.com/Atsushi776>
* <https://blog.atusy.net>

## dotfiles × 生産性

1. カスタマイズして、生産性を高める
    * ノウハウのコード化
    * 人のdotfilesの活用
2. 再現性・汎用性を高めて、生産性低下を予防する
    * 環境間の共有
    * 環境差異の吸収
    * セットアップの自動化
3. 布教して、他者の生産性に貢献する
    * OSS
    * Blog

atusyは1と3がメイン

## 個人的には再現性・汎用性はおまけ！

* 作りなおしやん！とか修正必要やん！ってなっても一過性
* そんな沢山の環境を管理していないなら予防は不要
* 都度対応で十分に予防力をつけられる
* でもかっこいいと思うし、必要な人もいるだろうし、やるのは全然あり！

## 個人的にはカスタマイズと布教がメイン！

* どちらも仕事術の整理
* カスタマイズは自分向けの最適化
* 布教は、他者も含めた一般化

## 課題から始めよう

* もう少し効率化したいな、引っかかりをなくしたいな、という自分の声に耳を傾ける
* この課題って自分だけのものじゃないのではと自問する

## 基本方針を手に入れよう

* 既存手段の自然な拡張 <!-- zoxide + ghq + vim-plugins -->
* 類推できる覚えやすさ <!-- tmux vs vim -->
* 定型操作への高速アクセス

## ディレクトリの移動の動線を減らす

* よく使うディレクトリにパターンがあるな
* `zoxide` を自然に拡張して統一
    * 使ったことあるディレクトリ（`zoxide`）
    * クローン済みGitリポジトリ（`ghq`）
    * Neovimプラグイン（`$HOME/.local/share/nvim/lazy/*`）

## tmux操作をVimっぽく

* tmuxの操作、覚えきれないけどやってることはVimに似てるな
* Vimを模倣して覚えやすく
    * pane移動を`M-w l`にすれば、Vimの`C-w l`っぽい！

```
bind-key M-w send-prefix
bind-key -n M-w switch-client -T vim-c-w
bind -T vim-c-w h select-pane -L
bind -T vim-c-w j select-pane -D
bind -T vim-c-w k select-pane -U
bind -T vim-c-w l select-pane -R
```

## treemonkey.nvim

- 範囲選択ってよく使うし確実にしたい
    - 関数の名前、定義全体など
- 既存手法だと一意な選択が難しいことある
- 一意じゃないところは選択肢を提示して選べるようにしよう

> Blog: オレのNeovim見て！ 2024
> <https://blog.atusy.net/2024/12/09/awesome-my-neovim/#範囲選択>

## jab.nvim

> Blog: オレのNeovim見て！ 2024
> <https://blog.atusy.net/2024/12/09/awesome-my-neovim/#行内の移動>


## agentic-scrum

https://github.com/atusy/agentic-scrum
