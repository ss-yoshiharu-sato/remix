---
title: Contributing
description: Thank you for contributing to Remix! Here's everything you need to know before you open a pull request.
---

# Remixへの貢献

私たちのゴールはRemixの開発が安定し、安定し、オープンであることです。ユーザーの素晴らしいコミュニティなしにはそれはできません！

このドキュメントでは、私たちの開発プロセスや、あなたの環境をセットアップする方法について説明します。

**あなたの作品が採用される最高のチャンスを確実にするために、投稿する前に必ずお読みください。**

## 貢献者ライセンス契約

Pull Requestを送信するすべてのコントリビューターは、コントリビューターライセンス契約（CLA）に署名する必要があります。

プルリクエストを開始すると、remix-cla-botはCLAをレビューし、あなたの名前を[contributors.yml][contributors_yaml]に追加して署名するように促します。

[CLAを読む][cla]。

## 役割

この文書では、以下の役割を持つ貢献者に言及している：

- **Admins**: 管理者権限を持つGitHubの組織チームは、ロードマップの設定と管理を行います。
- **Collaborators**: 書き込み権限を持つGitHubの組織チーム。課題、PR、ディスカッションなどを管理します。
- **Contributors**: 君だ！

---

## 開発プロセス

### Feature Development

新機能のアイデアがある場合は、Pull Requestを送らず、代わりにこのプロセスに従ってください：

1. 貢献者は、[GitHub Discussions][proposal]に**提案**を追加します。
2. Remixの**管理チーム**は、**ロードマップ計画**会議でプロポーザルを受け付けます。
   - 管理者がプロポーザルから**課題**を作成し、その課題を[**ロードマップ**][ロードマップ]に追加すると、プロポーザルが受理されます。
3. 管理者はissueに**所有者**を割り当てます。
   - オーナーは、API、動作、実装に関するすべての決定を含め、その機能を出荷する責任を負う。
   - オーナーは、より大きな問題のために、他の貢献者とともに作業を組織する。
   - オーナーは、Remixチーム内外からの貢献者である可能性があります。
4. オーナーはプロポーザルから**RFC**を作成し、開発を開始することができます。
5. 特に最初のうちは、ペアを組むことを強く推奨する。

### バグ修正プルリクエスト

もしバグを見つけたと思われるなら、それを修正するPRをお待ちしています！以下のガイドラインに従ってください：

1. コントリビューターは、プルリクエストに修正と一緒に失敗したテストを追加します。
   - 最初のコミットが失敗したテストであり、それを修正するコードの変更であれば理想的だ。
   - これは厳しく取り締まられるものではないが、非常にありがたい！
2. 管理者は、ロードマップ計画の一環として、未解決のバグ修正PRをレビューします。
   - 簡単なバグフィックスはその場でマージされる。
   - その他は、ロードマップに追加され、オーナーに割り当てられ、作業をレビューし、フィニッシュラインを通過させる。

テストケースのないバグ修正PRは即座にクローズされる可能性がある（テストが難しいものもあるので、ここでは慎重に判断する）。

### バグレポート問題

バグを見つけたが、PRを送る時間がない場合は、以下のガイドラインに従ってください：

1. Stackblitz、Replit、CodeSandboxなどのどこかに、問題の最小限の再現を作成し、私たちが訪問してバグを観察できるようにする：

   - [https://remix.new][https_remix_new]を使えば、本当に簡単だ。

2. これが不可能な場合（ホスティングの設定などに関連する）、バグを観察するための明確な指示をREADMEに記載し、私たちが実行できるGitHubレポを作成してください。

3. issueを開き、再現にリンクする。

再現性のないバグ報告は、再現性を求めて即座にクローズされます。

### ロードマップ計画会議

Remixの開発状況は、ライブストリーミングの企画会議でいつでもチェックできます：

- Remix管理者チームは毎週ミーティングを行い、進捗状況をコミュニティに報告し、提案と検証済みのバグをロードマップに追加します。
  - 提案書をロードマップに追加するには、Remix管理者の全会一致が必要です。
  - 提案は「却下」されるのではなく、ロードマップに「採用」されるだけである。
  - 投稿者は引き続き、提案に対するアップ・ヴォートとコメントを行うことができる。新しい動きがあれば、将来のレビューのためにバブルアップされる。
  - The Remix Admin team may lock Proposals for any reason.
- ミーティングの模様は[Remix YouTubeチャンネル][youtube]でライブストリーミングされる。
  - 会議が進行している間は、誰でも[Discord][ディスコード]`#roadmap-livestream-chat`に招待される。
  - リミックス・コラボレーターをご招待します。

### 問題追跡

ロードマップ課題の規模が大きくなることが予想される場合（複数のタスク、著者、PRなどを含む）、管理チームによって一時的なプロジェクトボードが作成されます。

- 当初の課題は、ロードマップ・プロジェクトに残され、全般的な進捗を確認することになる。
- サブタスクは一時プロジェクトで追跡される。
- 作業終了後、一時的なプロジェクトはアーカイブ化される。
- オーナーは、サブプロジェクトに課題を投入し、出荷可能な作業の塊に分割する責任がある。
- ビルド／フィーチャー・フラッグは、長期ブランチよりも推奨される。

### RFC

- 計画中のすべてのissueは、そのissueが_Planned_から_In Progress_に移行する前に、Official RFC DiscussionカテゴリにRFCが投稿されていなければなりません。
- 提案の中には、すでに十分なRFCとなっているものもあり、単に公式RFCの議論カテゴリに移動することもできます。
- RFCが掲載されれば、開発を開始することができるが、オーナーはコミュニティからのフィードバックを考慮し、必要に応じて方向性を変更することが求められる。

### オーナーへのサポート

- オーナーは[Discord][Discord]の`#collaborators`プライベート・チャンネルに追加され、アーキテクチャや実装に関するヘルプを得ることができます。このチャンネルは、管理者がメッセージを見逃さず、オーナーがブロックを解除できるように、雑音を最小限に抑えるためのプライベートチャンネルです。また、オーナーはどのチャンネルでもどこでもこれらの質問について議論することができます！
- 管理者はオーナーと積極的に協力し、課題やプロジェクトが整理され（正しいステータス、関連課題へのリンクなど）、文書化され、前進していることを確認します。
- 進捗が停滞している場合、issueのオーナーが変更されることがある。

### 週間ロードマップ・レビュー

週に一度、Remixチームと外部の**オーナー**がロードマップをレビューする。

- ブロッカーを特定する
- チームや地域社会でペアを組む機会を見つける

### 協力者の役割

リポジトリを清潔で整理された状態に保つため、コラボレーターは以下の行動をとります：

### 問題タブ

- 再現性のないバグ報告は、再現性を求めて即座にクローズされます。
- プロポーザルとなるべき課題は、プロポーザルに変換される。
- 質問は**Q&A Discussion**に変換されます。
- 有効な再現性のある問題は **Verified Bugs** と表示され、ロードマップ計画会議で管理者によってロードマップに追加されます。

### プルリクエストタブ

- 開発プロセス**を経ていないフィーチャーは即座にクローズされ、代わりにディスカッションを開くよう求められます。
- テストケースのないバグ修正PRは、テストを求めて即座にクローズされるかもしれません。(テストが難しいものもあります。コラボレーターはこのあたりを慎重に判断してください)。

---

## 開発セットアップ

コードベースに貢献する前に、レポジトリをフォークする必要があります。これは、どのような貢献をするかによって少し違ってきます：

以下の手順で、このリポジトリに変更を投稿するための設定を行います：

1. リポジトリをフォークする（[このページ][fork]の右上にある<kbd>Fork</kbd>ボタンをクリックする）。

2. ローカルにフォークをクローンする。

   ```shellscript nonumber
   # in a terminal, cd to parent directory where you want your clone to be, then
   git clone https://github.com/<your_github_username>/remix.git
   cd remix

   # if you are making *any* code changes, make sure to checkout the dev branch
   git checkout dev
   ```

3. `pnpm`を実行して依存関係をインストールする。npm` を使ってインストールすると、不要な `package-lock.json` ファイルが生成される。

4. Playwright をインストールして `npx playwright install` を実行するか、[Visual Studio Code プラグイン][vscode_playwright] を使用してテストを正しく実行できるようにします。

5. `pnpm test`を実行して、ローカルで開発するためのすべての設定が完了したことを確認する。

### Branches

**重要：** GitHubでPRを作成する際は、正しいブランチをベースに設定してください。

- **`dev`** コードの変更である。
- **`main`**: ドキュメントと一部のテンプレートの変更のため。

GitHub では、PR を作成する際に "Compare changes" の見出しの下にあるドロップダウンでベースを設定できます：

<img src="https://raw.githubusercontent.com/remix-run/react-router/main/static/base-branch.png" alt="" width="460" height="350" />

### テスト

このプロジェクトでは、テストに `jest` と `playwright` を混ぜて使っている。integrationフォルダに統合テスト一式があり、パッケージは独自のjestコンフィギュレーションを持ち、プロジェクトのルートにあるプライマリjestコンフィギュレーションから参照されます。

統合テストと一次テストは、`npm-run-all` を使って並列に実行することができます。これら 2 つのテストセットを個別に実行するには、個々のスクリプトを実行する必要があります：

- `pnpm test:primary`
- `pnpm test:integration`

プロジェクト、ファイル、テストのフィルタリングのためのウォッチプラグインもサポートしています。フィルタリングを行うには、 `--testNamePattern`, `--testPathPattern`, `--selectProjects` の組み合わせを使います。例えば

```shellscript nonumber
pnpm test:primary --selectProjects react --testPathPattern transition --testNamePattern "initial values"
```

また、ウォッチモードのプラグインも用意されている。pnpm test:primary --watch` を実行して `w` を押すと、利用可能なウォッチコマンドが表示されます。

あるいは、そのプロジェクトに `cd` して `pnpm jest` を実行することで、そのプロジェクトの jest 設定を完全に独立して実行することもできる。

## 開発ワークフロー

### パッケージ

Remixは複数のパッケージのコードをホストするためにmonorepoを使います。これらのパッケージは `packages` ディレクトリにあります。

[pnpm workspaces][pnpm_workspaces]を使用して、依存関係のインストールと各種スクリプトの実行を管理します。すべてをインストールするには、リポジトリのルートから `pnpm install` を実行してください。

### Building

ルートディレクトリから `pnpm build` を実行すると、ビルドが実行される。pnpm watch` を使えば、ウォッチモードでビルドを実行できる。

### Playground

アプリの機能開発中に実際のアプリとやりとりできるのは本当に便利なことが多い。そこで `playground` ディレクトリにアプリを置くと、ビルドプロセスが自動的に `playground` ディレクトリのすべてのアプリの `node_modules` にすべての出力をコピーしてくれる。また、ライブリロードイベントも発生する！

新しいプレイグラウンドを生成するには、単に実行する：

```shellscript nonumber
pnpm playground:new <?name>
```

プレイグラウンドの名前は任意で、デフォルトは `playground-${Date.now()}` である。そして、生成されたディレクトリに `cd` して `npm run dev` を実行する。別のターミナルウィンドウで `pnpm watch` を実行させれば、ライブリロードマジック 🧙‍♂️ を使って好きなRemixの機能に取り組む準備ができる。

`pnpm playground:new` から生成されるプレイグラウンドは `scripts/playground/template` にあるテンプレートに基づいています。テンプレートを変更したい場合は、`scripts/playground/template.local`にカスタムテンプレートを作成することができます。

### Testing

Before running the tests, you need to run a build. After you build, running `pnpm test` from the root directory will run **every** package's tests. If you want to run tests for a specific package, use `pnpm test:primary --selectProjects <display-name>`:

```shellscript nonumber
# Test all packages
pnpm test

# Test only @remix-run/express
pnpm test:primary --selectProjects express
```

## Repository Branching

This repo maintains separate branches for different purposes. They will look something like this:

```
- main   > the most recent release and current docs
- dev    > code under active development between stable releases
```

There may be other branches for various features and experimentation, but all the magic happens from these branches.

## How do nightly releases work?

Nightly releases will run the action files from the `main` branch as scheduled workflows will always use the latest commit to the default branch, signified by [this comment on the nightly action file][nightly_action_comment], however they check out the `dev` branch during their setup as that's where we want our nightly releases to be cut from. From there, we check if the git SHA is the same and only cut a new nightly if something has changed.

## End-to-end testing

For every release of Remix (stable, experimental, nightly, and pre-releases), we will do a complete end-to-end test of Remix apps on each of our official adapters from `create-remix`, all the way to deploying them to production. We do this by utilizing the default [templates][templates] and the CLIs for Fly, and Arc. We'll then run some simple Cypress assertions to make sure everything is running properly for both development and the deployed app.

[proposals]: https://github.com/remix-run/remix/discussions/categories/proposals
[roadmap]: https://github.com/orgs/remix-run/projects/5
[youtube]: https://www.youtube.com/@Remix-Run/streams
[discord]: https://rmx.as/discord
[contributors_yaml]: https://github.com/remix-run/remix/blob/main/contributors.yml
[cla]: https://github.com/remix-run/remix/blob/main/CLA.md
[fork]: https://github.com/remix-run/remix
[pnpm_workspaces]: https://pnpm.io/workspaces
[vscode_playwright]: https://playwright.dev/docs/intro#using-the-vs-code-extension
[nightly_action_comment]: https://github.com/remix-run/remix/blob/main/.github/workflows/nightly.yml#L8-L12
[templates]: ./templates
[https_remix_new]: https://remix.new
