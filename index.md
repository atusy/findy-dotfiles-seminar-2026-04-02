---
paginate: true
---

<style>
video,img {
  max-width: 100%;
  max-height: 100%;
  object-fit: contain;
  border: 1px solid #888;
}
a {
  color: #5555AD;
}
small {
  font-size: 0.8em;
}
strong {
  color: #AD5555;
}
h1 {
  font-size: 2em;
}
</style>


# dotfilesの整理は仕事術の整理！<br/>生産性向上まったなし！

<!-- https://findy.connpass.com/event/387107/ -->

## ![height:1em](images/headphone.jpg) atusy

---

## ![height:1em](images/headphone.jpg) atusy

- Engineering Manager兼Dev
- 好きなもの
    - Neovim
    - コーヒー（焙煎からやる）

---

## 著書: Rが生産性を高める (2022)

〜データ分析ワークフロー効率化の実践

![height:10em](https://gihyo.jp/assets/images/cover/2022/9784297125240.jpg)

---

## フォローよろしく！

- <https://x.com/Atsushi776>
- <https://blog.atusy.net>
- <https://github.com/atusy>

---

## dotfiles × 生産性

1. カスタマイズして、生産性を高める
    - ノウハウのコード化
    - 人のdotfilesの活用
2. 再現性・汎用性を高めて、生産性低下を予防する
    - 環境間の共有
    - 環境差異の吸収
    - セットアップの自動化
3. 布教して、他者の生産性に貢献する
    - OSS
    - Blog

atusyは1と3がメイン

---

## 個人的には再現性・汎用性はおまけ！

- 修正は一過性
- 環境が少なければ対処療法で十分免疫がつく
- でもかっこいいと思うし、必要な人もいるだろうし、やるのは全然あり！

---

## 個人的にはカスタマイズと布教がメイン！

- どちらも仕事術の整理
- カスタマイズは自分向けの最適化
- 布教は、他者も含めた一般化

---

## 課題から始めよう

- 自分に耳を傾ける
    - もう少し効率化したいな
    - 引っかかりがあるな
- 自分に問いかける
    - 満足してる？
    - この課題って自分だけのもの？

---

## 基本方針

自然さ ＞ 覚えやすさ ＞ 手早さ

- とにかく自然であること
    - 不自然さは思考を鈍らす
- 覚えにくいなら、覚えやすくするか、覚えなくてもよくする
    - 使ってないなら消す
- 面倒は使いながら改善する

---

## ディレクトリの移動の動線を減らす

- よく使うディレクトリにパターンがあるな
- `zoxide` を自然に拡張して統一
    - 使ったことあるディレクトリ（`zoxide`）
    - クローン済みGitリポジトリ（`ghq`）
    - Neovimプラグイン（`$HOME/.local/share/nvim/lazy/*`）

---

## tmux操作をVimっぽく

- tmuxの操作、覚えきれない
- やってることはVimに似てるな
- Vimを模倣して覚えやすくしよう
    - pane移動を`M-w l`にすれば、Vimの`C-w l`っぽい！

```tmux
bind-key M-w send-prefix
bind-key -n M-w switch-client -T vim-c-w
bind -T vim-c-w h select-pane -L
bind -T vim-c-w j select-pane -D
# 以下略
```

<small><https://github.com/atusy/dotfiles/blob/669bf2f3fe4cddd22937f2355a80eb9cf4151627/dot_tmux.conf?plain=1#L38-L52></small>

---

## テキスト選択を軽快に正確に

[atusy/treemonkey.nvim](https://github.com/atusy/treemonkey.nvim)

- 意味のある範囲をさくっと選択したい
    - 関数の名前、定義全体など
- 既存手法だと一意な選択が難しいことある
- 一意じゃないところは選択肢を提示して選べるようにしよう

> Blog: オレのNeovim見て！ 2024
> <https://blog.atusy.net/2024/12/09/awesome-my-neovim/#範囲選択>

---

## 思考に沿ってカーソルを動かす

[atusy/jab.nvim](https://github.com/atusy/jab.nvim)

- 読み上げている場所へさくっと移動したい
- 既存手法だと日本語対応に弱い
- migemoでASCII検索を日本語に拡張しよう

> Blog: オレのNeovim見て！ 2024
> <https://blog.atusy.net/2024/12/09/awesome-my-neovim/#行内の移動>

---

## agentic-scrum（WIP）

[atusy/agentic-scrum](https://github.com/atusy/agentic-scrum)

- AIに良い感じに開発してほしいがSDD（仕様駆動）は重い
    - 仕様が決まりきってない
    - 試すに値する最小の価値から育てたい
- それってウォーターフォールに対するアジャイルやん
- スクラム経験を活かして、agentic-scrumを作ってみよう

---

## Vibe codingの限界

- 明後日の方向に走ると、作業のほとんどが無駄になる
- 大量のコミットの人力レビューに限界がある

---

## AIでスクラムの限界を超える

- 人の制約から解き放て
    - タイムボックスは時間配分の最適化
        - AIの速度なら、時間より質
    - 定期イベントの調整
        - AIならスケジュール調整不要
- AIに最適なスクラムイベント再考

---

## dotfilesの先へ……

- dotfiles由来の生産性向上は作業効率アップにとどまらない
- 日常業務の生産性を向上させる力を手に入れろ！
    - 課題に気付く力
    - 課題を整理する力
    - 課題を解決する力
    - 課題を一般化する力
- dotfilesなら
    - 失敗できる
    - 時間をかけられる
    - 他者を模倣できる
