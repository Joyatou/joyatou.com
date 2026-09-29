# 画像の出典

架空題材の見本LP（ハカル勤怠）で使っている画像と、借りたアイコン・画面の部品の一覧です。

## 画面の画像

管理画面と打刻画面は、実在の製品のキャプチャではありません。架空サービス「ハカル勤怠」の画面を、下の表のTablerの部品（ナビゲーションの帯・カード・表・バッジ・ボタン・リストなど）でHTMLに組み、画像に焼いています。
文言・数字・従業員名はすべて架空です。

| ファイル | 使用箇所 | 元のファイル |
|---|---|---|
| app_pc.png | 最初の画面と、選ばれる理由の01（管理画面） | `作業/画面素材/app_pc.html`（Tablerで組んだもの）をChromeで2倍に焼いたもの |
| app_sp.png | 最初の画面・選ばれる理由の04（打刻画面） | `作業/画面素材/app_sp.html`（Tablerで組んだもの）をChromeで3倍に焼いたもの |

焼き直す手順は次のとおりです。

```
node ~/.claude/skills/jp-writing/scripts/render_at.js 作業/画面素材/app_pc.html --width 1440 --height 900 --dsf 2 --wait 2000 --shot site/img/app_pc.png
node ~/.claude/skills/jp-writing/scripts/render_at.js 作業/画面素材/app_sp.html --width 390 --height 844 --dsf 3 --wait 2000 --shot site/img/app_sp.png
```

## 借りた写真

素材サイトとウィキメディア・コモンズから、転載と商用の利用を許す条件の写真を借りています。
書き出しの時に撮影情報（EXIF）を消し、枠の幅に合わせて縮小しました。描き足しや消し込み、色味の調整はしていません。
CC BY-SAは表示が条件なので、実案件で流用する時は下の表示を残すか、撮影した写真に差し替えてください。

| ファイル | 使用箇所 | 取得元 | 作者 | ライセンス | 写真のページ |
|---|---|---|---|---|---|
| pickup.jpg | PICK UPの1つ目（ヘッドセット姿のオペレーター） | Unsplash | BaljkanN 4 | Unsplash License | https://unsplash.com/photos/wnpf3Q5pkXA |
| team.jpg | PICK UPの2つ目（3人の打ち合わせ） | ウィキメディア・コモンズ | 株式会社オンカ | CC BY-SA 4.0 | https://commons.wikimedia.org/wiki/File:92A0780.jpg |
| support.jpg | 選ばれる理由の03（モニター前の打ち合わせ） | Unsplash | Mimi Thian | Unsplash License | https://unsplash.com/photos/90u9nnhZwts |
| care.jpg | 導入事例2（小道でスマートフォンを操作する女性） | Unsplash | cal gao | Unsplash License | https://unsplash.com/photos/RpRH161AWcI |
| clock.jpg | 選ばれる理由の02（壁のカードリーダー） | Unsplash | Jakub Żerdzicki | Unsplash License | https://unsplash.com/photos/pLD-QID7x3k |
| office.jpg | 導入事例1（事務所の机に向かう女性） | Unsplash | phyo min | Unsplash License | https://unsplash.com/photos/P002vaEJlvk |

`pickup.jpg`・`team.jpg`・`care.jpg`・`office.jpg` の4枚は、枠の縦横比（4:3）に合わせて切り出してから縮小しました。`support.jpg` と `clock.jpg` は切り出していません。

写っている人は、導入企業の方でも、ハカルワークスのサポートの担当者でもありません。
Unsplashの利用規約（5. License to Images）は、写っている人の肖像を使う権利をライセンスに含めておらず、使い方によっては本人の許諾が要るとしています。
実案件では、導入企業やサポートの窓口で撮った写真（本人の同意つき）に差し替えてください。

### team.jpgの表示（CC BY-SA 4.0）

- 作品：92A0780（ウィキメディア・コモンズでの説明は「株式会社オンカのオフィス（2021年10月）」）
- 作者：株式会社オンカ
- ライセンス：CC BY-SA 4.0（表示-継承4.0国際）https://creativecommons.org/licenses/by-sa/4.0/deed.ja
- 元の写真：https://commons.wikimedia.org/wiki/File:92A0780.jpg
- 2026-09-28に、元の写真のページでCC BY-SA 4.0の表示を確かめました
- 手を加えたところ：元の写真（3000×2000px）の中央から2667×2000pxを切り出し、幅240pxに縮小しました
- この画像（team.jpg）も、CC BY-SA 4.0で提供します
- ページの末尾にも、作品・作者・ライセンスの表示を載せています

## 借りたアイコンと画面の部品

| 借りたもの | 使用箇所 | 版と読み込み先 | 利用条件 |
|---|---|---|---|
| Font Awesome Free | 上部と末尾の会社の印（clock）、携帯の幅のメニューのボタン（bars）、ご利用中の会社の印（gear・dove・mountain・print・sun・building）、お悩みの3つ（hourglass-half・building-user・gauge-high）、選ばれる理由の印（check）、機能一覧の8つ（id-card・calculator・circle-check・file-export・triangle-exclamation・book・calendar-plus・calendar-week）、最後の三つの窓口（file-lines・laptop・phone）、画面の画像の中の印（clock・battery-three-quarters）、ブラウザのタブに出る印（clock） | 6.7.2。CSSはcdnjs（https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.7.2/css/all.min.css）、タブの印はjsDelivr（https://cdn.jsdelivr.net/npm/@fortawesome/fontawesome-free@6.7.2/svgs/solid/clock.svg） | アイコンはCC BY 4.0、フォントはSIL OFL 1.1、CSSはMIT License（https://fontawesome.com/license/free）。表示は、読み込むCSSとSVGの中の著作権表示で足りる（配布物のLICENSE.txtの「Attribution」の項） |
| Tabler | 画面の画像2枚（`app_pc.png`・`app_sp.png`）の部品 | 1.6.0。jsDelivrのCSS（https://cdn.jsdelivr.net/npm/@tabler/core@1.6.0/dist/css/tabler.min.css）を `作業/画面素材/` のHTMLで読み込み、焼いた画像だけをページに置く | MIT License（https://github.com/tabler/tabler/blob/main/LICENSE）。著作権表示はCSSの先頭にある |
