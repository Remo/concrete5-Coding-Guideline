concrete5 コーディングガイドライン (5.7.x 以降)
concrete5.7.3.1 対応
更新 2015/4/9

# 本プロジェクトの仕様テンプレート

プロジェクトごとに設定する内容を記入ください

## 基本仕様 (例)

項目 | 内容
----|----
テーマハンドル | bsd
使用フレームワーク | Bootstrap / Foundation / 960Grid / オリジナル


## 使用ライブラリとバージョン (例)

プロジェクトで使用するライブラリとバージョンを記入してください

使用ライブラリ | バージョン
---- | ---
Bootstrap | 3.1.1
jQuery | 1.11.1
Bxslider | TBA


## ページテンプレートリスト (例)

Body Wrapper Class で出力を変更したいときに対応表として利用してください

名前 | ハンドル
--- | ---
p0_0 総合トップ | p0_0_top
p0_1 事業部トップ | p0_0_top_dept
p1_0 汎用 | default
p2_0 製品トップ | p2_0_product_top
p2_1 製品一覧 | p2_1_product_index
p2_2 製品詳細 | p2_1_product_detail

* 半角英大文字、半角英小文字、半角数字とアンダースコア(_)のみが使用可能です。
* アンダースコアー(_) は、Body Wrapper Class として出力されるときに、 **ハイフン(-) に自動変換** されます

## ページタイプリスト (例)

Body Wrapper Class で出力を変更したいときに対応表として利用してください

名前 | ハンドル | 使用ページテンプレート
--- | --- | ---
pt0_0 総合トップ | pt0_0_top | p0_0_top
pt0_1_1 ○事業部トップ | pt0_0_1_top_XX_dept | p0_0_top_dept
pt0_1_2 ○事業部トップ | pt0_0_2_top_XX_dept | p0_0_top_dept
pt0_1_3 ○事業部トップ | pt0_0_3_top_XX_dept | p0_0_top_dept
pt1_0_1 汎用一覧 | default_index | default
pt1_0_2 汎用詳細 | default_page | default
pt2_0 ライブラリトップ | pt2_0_product_top | p2_0_product_top
pt2_1_1 製品一覧 XXX | pt2_1_1_product_index_XXX | p2_1_product_index
pt2_1_2 製品一覧 XXX | pt2_1_2_product_index_XXX | p2_1_product_index
pt2_1_3 製品一覧 XXX | pt2_1_3_product_index_XXX | p2_1_product_index
pt2_2_1 製品詳細 XXX | pt2_1_1_product_index_XXX | p2_1_product_detail
pt2_2_2 製品詳細 XXX | pt2_1_2_product_index_XXX | p2_1_product_detail
pt2_2_3 製品詳細 XXX | pt2_1_3_product_index_XXX | p2_1_product_detail


* 半角英大文字、半角英小文字、半角数字とアンダースコア(_)のみが使用可能です。
* アンダースコアー(_) は、Body Wrapper Class として出力されるときに、 **ハイフン(-) に自動変換** されます


# 基本規則

- 文字コードは UTF-8 を使用
- 改行コードは LF (UNIX互換) を使用


# ファイルやアセットの保存場所

concrete5 では、テーマ関連のファイルを下記フォルダに保存しています。

バージョン | 保存先
--- | ---
concrete5.6.x | /themes/XXX/
concrete5.7.x | /application/themes/XXX

* XXX はテーマの識別ハンドル
* 半角英小文字と数字のみにしてくだい。英語大文字は使えません。
* 上記保存場所は自作テーマを保存する先です。パッケージ化をする場合は、「packages/XXX/themes/XXX/」以下となります。


## テーマ埋め込みのCSS, JS, 画像ファイルの保存場所

コーディングを行う時点で、テーマに埋め込む CSS や JS 画像ファイルは

- /application/XXX/css/
- /application/XXX/js/
- /application/XXX/images/

や

- /application/XXX/assets/css/
- /application/XXX/assets/js/
- /application/XXX/assets/images/

などとまとめられることを推奨します。


## HTML コーディング

HTML コーディングもモックアップなどは

- /application/XXX/html/

配下に設置し、同じ、css, js, 画像ファイルを読み込むように設定するとデバッグが用意になります。


# ライブラリについて

各バージョンのconcrete5 に同梱しているライブラリです。
同じライブラリを使用する場合は下記のバージョンを使用してください。

**特に jQuery は concrete5 と密接に関わり合っているので、競合する JavaScript を利用する際は、最新の注意を払ってください。**

ライブラリ名 |c5.6.3.3| c5.7.3.1
----- |---- | -----
ace | TBA | TBA
backstretch | TBA | TBA
bootstrap | 2.0.3 | 3.1.1
dropzone | N/A |
dynatree | N/A |
font-awesome | N/A  |
jquery | 1.7.2 | 1.11.1
jquery/fileupload |  |
jquery/form |  |
jquery/awesome-rating | N/A | TBA
jquery/ui | TBA | 1.10.3
jquery/visualize | N/A | TBA
jquery/touch-punch | N/A | TBA
kinetic | N/A | TBA
picturefill | N/A | TBA
redactor | N/A | TBA
select2 | N/A | TBA
select2_locale | N/A | TBA
underscore | N/A | TBA
select2 | N/A | TBA
spectrum | N/A | TBA
swfobject | N/A | TBA
TinyMCE | 3.5.11 | N/A

# CSS/JS フレームワーク

レスポンシブデザインなどを行う場合 concrete5 では下記のフレームワークに対応しています。

- Bootstrap
- Foundation
- 960Grid

どのフレームワークを決めかねている場合は Bootstrap をお使いください。

ただ concrete5 のバージョンによって concrete5 で使用している Bootstrap のバージョンが変わってくるので、ご注意ください。

Foundation をお使いの場合は UI の部分のハックが多少必要ですが、Bootstrap のバージョンには依存されません。


# CSS 命名について

## 禁止 & 注意事項

### body タグ禁止事項

#### body に ID や class を付けない (必須)

ページのデザインを変えるために Body タグに ID や class をつけることはしないでください。

#### body に Position を設定しない (必須)

Body には Position を設定しないでください。

#### Body には背景の設定をしない (推奨)

背景の設定は避けてください。
下記の Body Wrapper クラスで背景を指定するようにしてください。


## ccm- クラスを使わない (必須)

ccm-page というクラスを覗いて ccm-* というクラスは使用しないでください。これらは concrete5 が管理画面などのインターフェース用に使用しています。

## Body Wrapper クラス (必須)

concrete5.7.x では、下記の CSS クラスが組み込まれた <div> タグを <body> の開始直後と </body> 閉じタグの直前に挿入します。

- ccm-page
- page-template-XXX (XXX はページテンプレートのハンドル)
- page-type-XXX (XXX はページタイプのハンドル)

入れ子での CSS スタイルの適応を行う場合は、上記 class を活用できます。

高度な表現を行わない場合は、「page-template-XXX」や「page-type-XXX」のクラスは無視してコーディングを行ってください。

* ページテンプレートとページタイプのハンドルは半角英大文字、半角英小文字、半角数字とアンダースコア(_)のみが使用可能です。
* アンダースコアー(_) は、Body Wrapper Class として出力されるときに、 **ハイフン(-) に自動変換** されます
* ページタイプは「指定なし」が可能なため、page-type-XXX が出力されないパターンも想定可能です。


## Z-index について (必須)

Z-index は 1000 未満にしてください。

* concrete5.6.x は 5 未満


## ファイルのアップロード場所に依存しない (必須)

編集者が自由に画像をアップロードして使うような画像の場合、ファイルのアップロード位置に依存したコーディングは行わないでください。

- ユーザーが編集するブロック内部の画像はファイルマネーはーがランダムに生成したフォルダ内に格納されます。
- マイスオーバーで画像ファイル名の末尾に「_over」を付与する Javascript などは動作しません (* テーマ内にハードコーディングする場合を除きます)

## ブロックに ID を指定しない (強く推奨)

ブロックに ID を指定して表示するようなコーディングは避けてください。

## meta title, description, keywords, OGP タグ は不要 (推奨)

concrete5 側で挿入するため、不要です。

# 必須事項

## ページ上に表示されるすべての表示パターンを網羅してください。

- 仕様書、デザインデータを元に、必要な表示パターンすべてをコーディングしてください。
- 例：画像の左寄せ、中寄せ、右寄せなどの複数パターンが想定される場合はそのすべてのパターンのコーディングを行ってください。

## トルツメの対応

- 要素が未入力の場合、トルツメにすることによって表示が崩れるようにしないでください。
- 例：ページリストのサムネイル画像がない場合、ページタイトルの表示部分が崩れないようにする。

## 繰り返し表示予定の箇所の対応

- 同じ要素を繰り返し出力する箇所では、要素の増減により、表示崩れなどが発生しないようにしてください。
- グリッド表示を行う場合、横1列、縦1列ごとに div で囲むような入れ子処理はせずに、そのブロック全体で div を囲むようにしてください。
- 必ず繰り返した状態でコーディングしてください
- 必要であれば、要素が全くない状態を考慮してください。場合によっては別のコーディングを出力する必要がある場合があります。カスタマイズで対応できるので、事前に concrete5 実装者と可能かどうか相談してください。
    - 例：0個の時、トルツメにするのか別の表示にするのか
    - 例：1個のとき、 スライドショーで自動再生をするが、画像が1個しかないとき自動再生があるため同じ画像でエフェクトが繰り返されてしまう場合の対処

## 繰り返し要素のサイズの考慮

- グリットデザインなど縦の位置を他の要素と合わせないといけない場合は、できれば JS などで縦の高さを調整するように設定してください。
- 不可能であれば横1列ごとに1つのブロックを追加するように対処するので運用を検討してください。
- 例：ページリストで、サムネイル画像、日付、ページタイトルの3要素が横に並んでいる場合、サムネイル画像がなかった時、表示崩れが起きてしまう。


## テキストの増減への対応

入力文字数が増減することを想定して、表示崩れが起きないようにしてください。

- 例：画像の回り込みの増減で、少ない時に clearfix がないため、次の要素とかぶる
- 例：ページリストで、サムネイル画像、日付、ページタイトルの3要素が横に並んでいる場合、ページタイトルが2行になる時に、表示崩れが起きてしまう。


# 奨励事項

## ブロックのコーディングが、ブロック単位でデザインが再現し、できるだけ汎用的になるようにしてください

- ブロックはエリアに自由に配置できます (上級権限モードなどで制限は可能)
- そのエリアだけにしか使えないようにするなど、特定の場合を除く、ブロック外の class から継承するようなことは避けてください。

## BEM (Block Elements Modifier)

ページの枠をコーディングする際、BEM のコンセプトに基づいてコーディングをされることを推奨します。

参考記事
https://app.codegrid.net/entry/bem-basic-1


## LESS の使用

concrete5.7.x では、LESS のコンパイラーを内蔵しています。
HTMLコーディングを確認する際は、コンパイルが必要ですが、concrete5 ではコンパイルが必要ありません。

CSS プリプロセッサーを使用する際は LESS を採用されることをおすすめしますが、必須ではありません。

# 各ブロックのコーディング仕様

## 記事ブロック

デフォルト：囲む div など何もなし

推奨：記事ブロックは一つのブロック全体を `<div class="wysiwyg"></div>` で囲むようにして中身のタグはなにも class を指定しないようにしてください。この場合、記事ブロックのオーバーライドのカスタマイズが必要になります。（追加費用？）

どうしても指定が必要な場合や `<span>` を間に挟まないといけないような場合は、更新者がコーディングの知識をある程度持ち合わせている場合か、一定の法則があれば JS で対応するようにしてください。

下記が、記事ブロックから排出した HTML コーディングのサンプルです。
下記のコードを参考に CSS の調整をしてください。


``` 記事ブロックサンプル.html
<div class="wysiwig"> <!-- この div タグは concrete5 標準ではありませんがコンクリートファイブジャパンが推奨する方法です。記事ブロックをオーバーライドする必要があります。-->
    <p>P</p>

    <h1>H1</h1>

    <blockquote>
        Blockquote
    </blockquote>

    <p><strong>Strong</strong></p>

    <p><em>Italic</em></p>

    <p><u>Underscore</u></p>

    <p><del>Strikethrough</del></p>

    <p>UL&nbsp;List</p>

    <ul>
        <li>UL List</li>

        <li>UL List</li>

        <li>UL List</li>
    </ul>

    <p>OL List</p>

    <ol>
        <li>OL List</li>

        <li>OL List</li>

        <li>OL List</li>
    </ol>

    <p>No&nbsp;Indent</p>

    <p style="margin-left: 20px;">1 Indent</p>

    <p style="margin-left: 40px;">2 Indent</p>

    <p>Image</p>

    <p><img src="http://sakan.concrete5japan.net/index.php/download_file/view_inline/13"></p>

    <p>Align Left</p>

    <p>Align Right</p>

    <p>Table</p>

    <table>
        <thead>
            <tr>
                <td>Head</td>

                <td>Head</td>

                <td>Head</td>
            </tr>
        </thead>

        <tbody>
            <tr>
                <td>1</td>

                <td>2</td>

                <td>3</td>
            </tr>

            <tr>
                <td>1</td>

                <td>2</td>

                <td>3</td>
            </tr>
        </tbody>
    </table>

    <p><a href="/index.php?cID=1" data-concrete5-link-type="ajax">Internal Link</a></p>

    <p><a href="/index.php/download_file/view/1" data-concrete5-link-type="image" data-concrete5-link-launch="lightbox-image">Light box Link - Image</a></p>

    <p><a href="/index.php?cID=1" data-concrete5-link-type="ajax" data-concrete5-link-launch="lightbox-image">Light box Link - AJAX</a></p>

    <p><a href="/index.php/download_file/view/1" data-concrete5-link-type="image">File Download Link</a></p>

    <p>Align Text to the Left</p>

    <p style="text-align: center;">Center text</p>

    <p style="text-align: right;">Align text to the right</p>

    <p style="text-align: justify;">Justify Text</p>
    <hr>

    <p><span style="color: rgb(192, 80, 77);">Font color</span></p>
</div>
```

## HTMLブロック

HTML ブロックはデフォルトでは

`<div id="HTMLBlockXXX" class="HTMLBlock">`

という、ブロックの識別数字がついた ID と HTMLBlock という Class を div で囲って表示します。

コーディングの場合によってはオーバーライドをして、この div を表示しないようにする必要があります。

## オートナビブロック

ul li で構成するナビゲーションブロックです。

- 階層で分けることが可能
- グローバルナビなどで使用
- メガメニュー表示なども追加カスタマイズで可能
- パンくずの表示も可能

div などを新たに囲む必要がある場合なども可能
ただし、閉じタグなどのパターンを考えるときに複雑になりかねないので、ul li のみで構成できるように極力努力する。

## ページリストブロック

表示できる要素

- ページタイトル
- 日付
- サムネイル画像
- その他任意のページ属性
    - トピックラベル
    - 選択肢など

ブロック全体を大きく div で囲み、ひとつのページ情報に対して一つの繰り返し要素としてコーディンづする。

ページ送りについては、特定のコーディングで対応することが必要 ( **準備中** )


## イメージスライダーブロック

表示できる要素

- 画像
- タイトル
- WYSIWYG (記事ブロック)
- リンク

ページリストブロックのコーディング方法と基本的に同じ。
JS ライブラリを使う場合は、concrete5 標準JSライブラリとコンフリクトを起こさないようにする。

ブロック内でサムネイル画像一覧を表示し、画像のページ送りなどを行う場合は、ブロック側ではサムネイル画像を全部表示し、画像送り部分は JS で処理する。

## FAQ ブロック

要素(作成中)

- タイトル(テキストのみ)
- WYSIWYG (記事ブロックと同じ)