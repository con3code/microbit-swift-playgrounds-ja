# micro:bit Swift プレイグラウンド

## 概要

このドキュメントは、あなた自身の Swift プレイグラウンドブックを作成するために BBC micro:bit テンプレートブックを使用する方法をカバーします。プレイグラウンドブックのフォーマットやContent.swiftファイルのマークアップに関する詳細は含まれていません。

用語_Swift Playground_は異なる意味を持つことができます。Swift Playground に言及するとき、私たちは _Swift Playground Book_ を意味します。ブック形式では、ブック形式で構成されるような章やページを作成することができます。

Swift Playgroundのブックフォーマットの完全な説明については、[Appleのドキュメント][playground_link]を参照してください。あなた自身の本を作ろうとする前に、このドキュメントに慣れるべきです。

[playground_link]:https://developer.apple.com/documentation/swift_playgrounds?language=objc

## micro:bitテンプレートブック

Swift Playgroundをゼロから作成するのは複雑なプログラミング作業です。テンプレートブックを提供することで、Bluetoothでmicro:bitとペアリングして通信するために必要な複雑なコードを全て書きました。テンプレートブックは、Playground SDK（ソフトウェア開発キット）を提供すると考えることができます。

テンプレートブックはこのリポジトリで**micro-bit template.playgroundbook**として提供されています。

このフォルダーをクローンした後、適切な名前に変更する必要がありますが、拡張子は**.playgroundbook**のままにしてください。

Mac OSコンピュータ上では、これは_bundle_ファイルとして表示されます。つまり、1つのファイルとして表示されますが、実際にはディレクトリ構造になっています。ディレクトリ構造を開くには、ブックを選択し、Finderのコンテキストメニューから**パッケージの内容を表示**を選択する必要があります。

ブックを編集するには、理想的にはSwiftとplistファイルの編集に適したツールが必要です。Apple App StoreからXcodeをダウンロードすることをお勧めします。

編集する必要のあるファイルは**Contents/Chapters/**にあります。また、適切な**manifest.plist**ファイルを編集する必要があります。詳細は[Appleドキュメント][playground_link]を参照してください。

Contents/Sources**ディレクトリの中には、プレイグラウンドがmicro:bitと通信するために必要なすべてのソースファイルと、その他のサポート機能のホストがあります。これらはまた、私たちのSwift Playground SDKの機能性への追加の洞察を提供するかもしれません。

## 本のテスト
あなたの本をテストするために、あなたはどちらかをすることができます：

* iCloudドライブの**Playgrounds**フォルダにコピーしてください。iPadのSwift Playgroundsアプリは、それが追加/更新されたことに気づき、それに応じてダウンロードします。
* FinderからiPadにプレイグラウンドブックをエアドロップし、iPad上で対応する。この方法は、最初に本をコピーするときは良いのですが、それ以降にドロップすると、本のコピーが作成され、時間が経つにつれて蓄積され、削除する必要があります。
* 以下に詳しく説明するスクリプトファイルを利用するか、Automatorアクションを作成してください。

Appleのドキュメントには、プレイグラウンドをデバイスに取り込むさまざまな方法も掲載されています。

## micro:bit API Book

このリポジトリには**microbit API.playgroundbook**という別のSwiftプレイグラウンドブックも含まれています。

このプレイグラウンドは、micro:bit と対話するために定義した API 全体のインタラクティブなデモンストレーションを提供します。Swift Playgroundsアプリから可能な多くの可能性を説明するので、あなた自身の本を開発する前に、これをiPadにインストールして探索することを望むかもしれません。

## スクリプトファイルの使用

リポジトリには3つのスクリプトファイルも含まれています：

* create_doc_book.sh
* create_intro_book.sh
* create_template_book.sh

これらは、**micro:bit API**, **Intro to the BBC micro:bit** and **micro-bit template** playground booksを作成するために使用しました。これらのスクリプトは**micro-bit source**ブックをコピーしてコンパイルし、ブックの内容を別々のフォルダからマージします。これらのスクリプトのいずれかをコピーし、あなた自身のワークフロー用に変更することができます。これらのスクリプトには、オリジナルのストーリーボードとアセットをソースブックからコンパイルする行が含まれています。ストーリーボードやアセットを修正するつもりがなければ、代わりにコンパイルされたテンプレートブックから作業してください。

## 行動規範

信頼、パートナーシップ、シンプルさ、そして情熱は、私たちが日々の仕事やプロジェクトで実践している基本的な価値観です。私たちのオープンソースプロジェクトも例外ではありません。私たちは、世界中にまたがる活発なコミュニティを持ち、誰もが私たちのプロジェクトに参加し、貢献することを歓迎し、奨励しています。私たちは、前向きでオープン、包括的で協力的な環境の醸成に努めており、コミュニティがmicro:bitの行動規範を尊重することを信頼しています。私たちの[行動規範](https://microbit.org/safeguarding/)をご覧ください。私たちのコミュニティに参加するすべての人々に対する私たちの期待や、懸念事項の報告方法、違反が発生した場合の詳細が記載されています。
