+++
date = '2025-08-23T09:40:49+08:00'
draft = false
title = '我為什麼使用 Emacs'
slug = 'why-i-use-emacs'
+++

![](https://download.logo.wine/logo/GNU_Emacs/GNU_Emacs-Logo.wine.png)

我從兩年前開始用 Emacs——我通常用它來寫文章（包括目前這篇）、寫程式、問 AI 問題，用起來非常爽。但是，我周圍的人幾乎都不理解——他們覺得 Emacs 很慢、老、而且很奇怪（可能最後一點是對的）。

所以，我想來說說我使用 Emacs 作為主力 text editor （和系統）的理由。

## Flexibility

![](https://github.com/emacs-tw/emacs-101-beginner-survival-guide/raw/master/pic/alliances_zh.png)

Emacs 允許你做**任何你想要的事**——**真的，就是字面上的意思**。

- 不喜歡 modeline？自己刻！
- 想看 YouTube 影片？裝個 [瀏覽器的 package](https://github.com/emacs-eaf/eaf-browser)。
- 覺得 Emacs 很 BLOATED？把不要的 package 砍掉！

你有權利修改 Emacs 裡的**任何**東西。對，**任何**！

比起普通的 text editor，Emacs 更像是一個可以任意客製化的作業系統。

Emacs Lisp （Elisp）是 Emacs 的核心和魅力所在。Emacs Lisp 是 Emacs 的 configuration language，是一個完整的程式語言，也是 Emacs 和其他編輯器差異最大之處。

一般的 text editor（比如 VSCode、Sublime Text、Zed）通常是 out of box，安裝完即可使用，configuration language (通常是 JSON、TOML）的存在是為了讓使用者小修小改。想開發自己的 plugin？ 可以，但你得用另外一個語言（Python、JavaScript）。

Emacs 則不然。Emacs 的 core 為一個由 C 寫成的 Emacs Lisp interpreter，剩下所有的功能都是用 Emacs Lisp 寫成的。而 Emacs 也讓你能用 Emacs Lisp 隨意調整 Emacs，**一切細節都公開透明**。對於你不喜歡的預設功能，你總可以用 Emacs Lisp 改個變數、跑個 function 修改（或自己從頭寫！）。只要**五分鐘**，任何人都能輕鬆寫出一個 package & 使用。

而且自從教主 RMS （Richard Stallman）在 1984 年開發出 GNU Emacs 第一版以來，Emacs Lisp 幾乎沒有太大的改動——這代表**你二十年前用 Emacs Lisp 寫的 package 到現在還能用**！舉個現實的例子，目前 Emacs 最有名的 package [Org Mode](https://orgmode.org) 便是二十年前一個教授所寫的。

過去二十年來，無數 Emacs 高手寫了優秀、強大的 package。這些 package 很多都放在 [MELPA](https://melpa.org/#/) 上，只要 `M-x package-install package` 就可以安裝使用。這些 package 就只是一個個 Emacs Lisp file，所以你也可以更改、研究背後的功能。只要你電腦上有 Emacs，**這些 package 都能用一輩子**！

只要花幾個小時投入，你就能獲得一個**真正屬於你的 text editor**。

## Power

![](https://imgs.xkcd.com/comics/real_programmers.png)

一個配置好的 Emacs 可以是：

- 一個完全不用滑鼠、更不吃 RAM 的 VSCode + Terminal
- 一個可以 auto-complete 英文單字的 Markdown Editor
- 一個可以任意切換 Model、搜尋對話記錄的 LLM Client
- 、、、

這可不是一般 text editor 能做到的。

## Keyboard-Driven

![](https://img-9gag-fun.9cache.com/photo/37474_460s.jpg)

Emacs （和宿敵 Vim）皆是上個世紀文字介面時代的產物，所以你使用 Emacs 時可以完全不碰滑鼠，純粹依靠鍵盤來輸入、移動，達到極高的編輯效率。

網路上有不少人批評 Emacs 傷手——這實際上也算事實，Emacs 內建的快捷鍵真的不是給一般人用的。

但是有一群 Emacs hacker 寫了 [Evil](https://github.com/emacs-evil/evil) 。Evil 讓你可以在 Emacs 用 Vim 的 keymaps（我知道聽起來有點邪教），體驗上和 Neovim/Vim 幾乎毫無差異！而 [general.el](https://github.com/noctuid/general.el) 可以實現 Vim 中的 leader keys，設定上比 Neovim/Vim 那套方法更好理解。

我目前的 Emacs 就定義了好幾個 shortcuts:

- `SPC f f` 搜尋檔案
- `SPC m s` 開啟 Magit (一個 Git 前端）
- `SPC g g` Ripgrep 搜尋特定關鍵字
- `SPC c p` 編譯、輸入測資、執行 C++ 程式（競程）

再舉個例子，我時常使用 Gemini、ChatGPT 問程式問題。

在 VSCode 中，如果我想打開 GitHub Copilot 問問題，我必須用滑鼠打開右邊的 tab、輸入 prompt、再用滑鼠複製回答。

但在 Emacs 中，我可以直接 `SPC g p` 開一個空的 chat、輸入完問題按 `C-C return` 得到答案，再用 Vim keymap 複製答案。整個過程不用滑鼠，也快上不少。

## 總結

試試看 Emacs 吧。可以用用看我的 [emacs.d](https://codeberg.org/yubaitw/emacs.d)，或是用成熟的 configuration （比如 [Doom Emacs](https://github.com/doomemacs/doomemacs)）。

你會喜歡上 Emacs 的 :)
