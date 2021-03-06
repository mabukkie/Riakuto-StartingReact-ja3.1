<!-- markdownlint-disable MD024 -->
# 各版における内容の変更

## 第3.1版（2020-12-26）

### アップデート

- 主なパッケージの対応バージョンを以下にアップデート
    - **React**　17.0.0 RC1 → 17.0.1
    - **Create React App**　3.4.3 → 4.0.1
    - **TypeScript**　4.0.2 → 4.1.3
    - **ESLint**　6.8.2 → 7.14.0
    - **React Query**　2.15.4 → 3.5.5
- 引用している npm trends の各グラフを 2020 年 12 月現在のものにアップデート

### 呼称の変更

- 「ビルトインオブジェクト」と表記していたものを「組み込みオブジェクト」に変更
- 「Mac OS」と表記していたものを「macOS」に修正
- 「Visual Studio Code」の略称表記を「VSCode」から「VS Code」に修正
- TypeScript の「ユニオン型」を「共用体型」に、「インターセクション型」を「交差型」に変更

### 第1章&nbsp; こんにちは React

- 「1-1. 基本環境の構築」節の「Node.js をインストールする」項にて、従来 Mac のみで説明していた環境作成について Windows でのケースも言及。**WSL をベースにした Windows での環境手順**を[オンラインドキュメント](./extra/build-win-env.md)として追加した
- 「1-3. アプリを管理するためのコマンドやスクリプト」節「Yarn コマンド」項にて、プロジェクトパッケージのロックファイルについて、npm コマンド使用時の `package-lock.json` についても言及

### 第4章&nbsp; TypeScript で型を強める

- 「4-5. さらに高度な型表現」の「型表現に使われる演算子」項にて、配列の要素から型を作成する書き方の説明を追加
- 「4-5. さらに高度な型表現」節に新しく「**条件付き型とテンプレートリテラル型**」項を追加
- 「4-5. さらに高度な型表現」節の「組み込みユーティリティ型」項にて、`Record` 型および文字列リテラルの各ユーティリティ型についての説明を追加

### 第5章&nbsp; JSX で UI を表現する

- [**新しい JSX 変換形式**](https://ja.reactjs.org/blog/2020/09/22/introducing-the-new-jsx-transform.html) についての説明を随所に追加

### 第6章&nbsp; Linter と フォーマッタでコード美人に

- 「6-1. ESLint」節の内容を ESLint 7 に対応したものにアップデート
- 「6-2. Prettier」節「ESLint のプラグインとして Prettier をインストール」を「Prettier の環境を作る」に変更。[Prettier 公式が eslint-plugin-prettier を非推奨とした](https://prettier.io/docs/en/integrating-with-linters.html#notes)ため、**Prettier  を ESLint のプラグインではなく直接実行する形式**での環境構築に内容を変更

### 第12章&nbsp; React は非同期処理とどう戦ってきたか

- Recoil を使ったサンプルコードを収録

### 第13章&nbsp; データ取得の次世代標準 Suspense

- React Query に関する説明をバージョン 3.2 以降のものにアップデート
- 「13-4. Suspense と Concurrent モードが革新する UX」節にて、`useTransition` および `useDeferredValue` の設定オプションから `timeoutMs` が削除されたため、説明もそれに合わせて変更
- 「13-4. Suspense と Concurrent モードが革新する UX」節「Concurrent モードで先進的 UI を実現する」項にて、error boundary のリセットに React Query の `useQueryErrorResetBoundary` を使ったサンプルを追加

## 第3版（2020-08-20）

### 第1章&nbsp; こんにちは React

- 「1-1. 基本環境の構築」にて Node.js そのものと、インストールが必要な理由についての説明を追加
- 同じく「1-1. 基本環境の構築」にて、非推奨になった [ndenv](https://github.com/riywo/ndenv) を [nodenv](https://github.com/nodenv/nodenv) に置き換えた。併せて、[anyenv-update](https://github.com/znz/anyenv-update) と [nodenv-default-packages](https://github.com/nodenv/nodenv-default-packages) のふたつのプラグインを導入
- 同じく「1-1. 環境構築」にて、`yarn upgrade-interactive` コマンドの説明を追加
- 「1-2. Hello, World!」を「1-2. プロジェクトを作成する」に再編成。Create React App についての詳細な説明を追加し、Yarn コマンドの説明については次の節に委譲した
- 「1-3. アプリを管理するためのコマンドやスクリプト」節を新規に追加。Yarn コマンドに加え、npm-scripts や react-scripts についても詳細に説明

### 第2章&nbsp; エッジでディープな JavaScript の世界

- 章題を「ナウでモダンな JavaScript」から変更し、内容を全体的に再構成。ボリュームも従来の 5 倍以上に
- 「2-1. あらためて JavaScript ってどんな言語？」で JavaScript の成り立ちから立ち戻って概要の説明を追加
- 「2-3. JavaScript のデータ型」の節を新規に追加
- 「2-4. 関数の定義」にて、宣言文と関数式のちがいの説明、アロー関数で引数がひとつのときの括弧を省略するべきかどうかの議論を追加。さらに「引数テクニック」の項を追加
- 「2-5. クラスを表現する」にて、プロトタイプベースについての説明を追加
- 旧「2-6. 非同期処理を扱う」を第3章に「3-4. JavaScript での非同期処理」として移動
- 「2-8. JavaScript の鬼門、this を理解する」を新規に追加
- 「2-9. モジュールのインポート／エクスポート」を追加。`import` と `export` の使い方に加え、ESM 周辺の特殊事情についても説明

### 第3章&nbsp; 関数型プログラミングでいこう

- 「3-1. 関数型プログラミングは何がうれしい？」にて、実際のサンプルコードを使った説明を追加
- 「3-2. コレクションの反復処理」にて、`Array.prototype.reduce()` と `Array.prototype.sort()` についての説明を別途詳細に。またオブジェクトの反復処理についても新規に項を設けて説明
- 「3-3. 関数型プログラミングの概要」「3-4. 高階関数」「3-5. クロージャ」の節を「3-3. JavaScript で本格関数型プログラミング」として統合
- 旧「3-6. ジェネレータ」の節を削除、簡略化した説明を第11章の「自走式重対空砲 redux-saga」にあらためて記述
- 2章から内容を移動した「3-4. JavaScript での非同期処理」にて、説明とサンプルコードを全て刷新。`Promise` オブジェクトの作成法から始まり、通信ライブラリが返す `Promise` オブジェクトを扱う実践的な内容に

### 第4章&nbsp; TypeScript で型を強める

- 章題を「型のある TypeScript は開発者の味方」から変更し、内容を全面的に再構成。ボリュームも従来の3倍以上に
- 旧「4-3. 配列とオブジェクト」の内容は「4-4. 型の名前と型合成」に吸収
- 旧「4-5. コンパイル設定」の内容は「4-8. TypeScript の環境設定」に吸収
- 「4-3. 関数とクラスの型」「4-5. さらに高度な型表現」「4-6. 型アサーションと型ガード」「4-7. モジュールと型定義」の4つの節を新規に追加

### 第5章&nbsp; 強力な拡張記法 JSX

- 「5-1. JSX とは何であるか、何ではないのか」で引用している統計指標をアップデートし、説明をよりくわしく拡充

### 第6章&nbsp; Linter とフォーマッタでコード美人に

- 「6-1. ESLint」で JavaScript および TypeScript における linter の歴史を紹介。さらに  `yarn eslint --init` から始める設定ファイル作成の方法、各プラグインや共有設定、カスタマイズしているルール、ESLint を無効化するコメントの書き方についても新しく追加
- 「6-2. Prettier」で Prettier の登場背景を紹介。インストールの方法の説明を追加。設定の内容も紹介
- 「6-3. stylelint」として stylelint についての説明を独立させた

### 第7章&nbsp; React をめぐるフロントエンドの歴史

- 章として新しく追加。

### 第8章&nbsp; 何はなくともコンポーネント

- 従来の「7-1. React の基本思想」の内容を第7章に吸収、新しく「8-1. コンポーネントのメンタルモデル」に差し替えた
- 章全体で関数コンポーネントをベースにして、クラスコンポーネントをその対比で説明するという形に変更したため、「7-5. 関数コンポーネント」節を削除

### 第9章&nbsp; Hooks、関数コンポーネントの合体強化パーツ

- 「9-1. Hooks に至るまでの物語」を追加。mixins、HOC、render props と順を追ってロジックの再利用の歴史を説明。
- 「9-4. Hooks におけるメモ化を理解する」を追加、Hooks のメモ化について 1 節をさいて説明。

### 第10章&nbsp; React におけるルーティング

- 「10-2. ルーティングライブラリの選定」で Reach Router についての説明を追加。さらに将来の React Router との統合プランについて記述
- 旧版「10-3. React Router の使い方」の、サンプルコードを利用した説明の部分を「10-4. React Router をアプリケーションで使う」として独立させた
- 「10-5.  React Router バージョン 5 から 6 への移行」節を新規に追加

### 第11章&nbsp; Redux でグローバルな状態を扱う

- 「11-1. Redux の歴史」で、Redux 登場時の状況の描写をより詳細に
- 「11-2. Redux の使い方」の内容とサンプルコードを HOC から Hooks インターフェースを使ったものに更新
- 「11-3. Redux 公式スタイルガイド」「11-4. Redux Toolkit を使って楽をしよう」「11-5. Redux と useReducer」を新規に追加

### 第12章&nbsp; React は非同期処理とどう戦ってきたか

- 第12章を「React は非同期処理とどう戦ってきたか」に改題。前版の内容を書き直した上で、新しく「12-2. Effect Hook で非同期処理を書く」「12-3. Redux 不要論を検証する」節を追加

### 第13章&nbsp; データ取得の次世代標準 Suspense

- 章として新しく追加

<br />

## 第2版（2019-04-14）

- Create React App 本家が TypeScript を直接サポートし、[create-react-app-typescript](https://github.com/wmonk/create-react-app-typescript) はパッケージそのものが非推奨になったため、create-react-app-typescript を使用していた部分を create-react-app に入れ替えた
- 「2-5. 便利な配列やオブジェクのトリテラル」に、分割代入についての説明を追加
- 「3-5. クロージャ」の章を追加
- 「3-6. ジェネレータ」の章を追加
- 「4-2. 型のバリエーション」に、never型についての説明を追加
- 「4-3. 配列とオブジェクト」の交差型と共用型についての説明の誤りを訂正。および TypeScript 3.4 から導入された Readonly 型についての説明を追加
- 「4-5. コンパイル設定」に、絶対パスインポートについての説明を追加
- TypeScript の構文チェックツール TSLint については ESLint への統合プランが発表され1、近い将来に非推奨になるとアナウンスがあったため、「6-1. TSLint」の内容を「6-2. ESLint」に変更。加えて全てのサンプルコードの TSLint の環境を ESLint に移行
- 「7-5. 関数コンポーネント」で Stateless Functional Component（SFC）の呼称を Function Component（FC）に変更
- Hooks が導入され Recompose の開発中止が宣告されたため、第8章の内容を「合成するぞ Recompose」から「Hooks で関数コンポーネントを強化する」に置き換える形で刷新
- 「10-3. Reduxの使い方」で、最新のReduxおよびReact Reduxに対応した型解決の記述法に切り替えた
- TypeScript FSAの更新が滞っているため、「10-4. Flux Standard Action」の内容をTypeScript FSAを使わない手法を使ったものに書き換えた
- 「10-5. Redux DevTools」の内容を[『りあクト！ TypeScriptで極める現場のReact開発』](https://oukayuka.booth.pm/items/1312815)に委譲
- 「第11章 Reduxで非同期処理を扱う」の内容を追加
- その他使用している主なパッケージを、2019年3月時点の最新バージョンにアップデート
