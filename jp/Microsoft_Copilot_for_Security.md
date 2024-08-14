# Microsoft Copilot for Security

## 概要
- 生成AIを利用したクラウドベースのセキュリティ分析ツール
- 自然言語で要求を行い、テキスト・画像・ドキュメントの形式で応答を出力する
- 既存のツールやプロセス、ナレッジベースと接続し、応答を作成する際に参照してもらうことができる。
## 用語
- セッション：Copilot内の特定の会話
- プロンプト：セッション内の特定の質問（ステートメント）
- プラグイン：Copilotに組み込み可能な機能の集合（ツールやサービス）
  - Microsoft Defender XDR
  - Splunk など
## 主な使い道
- インシデントの概要の要約
- インシデントの影響分析
- スクリプトのリバースエンジニアリング
- インシデント対応に関するガイド付きの応答
## 機能
### スタンドアロン エクスペリエンス
#### Copilotランディングページ（ポータル）
![image](https://github.com/user-attachments/assets/73721ecc-8aac-4f7b-b0a1-b10e6fc7798e)
##### 主な構成要素
- **ハンバーガーメニュー**
  - ホーム
  - マイセッション
    - 過去のセッション（Copilot内の会話）一覧
  - プロンプトブックライブラリ
    - 組み込みプロンプトブックとカスタムプロンプトブックを含む
    - 選択したプロンプトブックを実行可能
  
  - 所有者設定（「ロール：所有者」のユーザのみ）
  - ロールの割り当て（「ロール：所有者」のユーザのみ）
  - 使用状況の監視（「ロール：所有者」のユーザのみ）
  
  - 設定
    - ユーザ設定
    - データとプライバシー
    - その他（アプリのバージョン情報）
  - アカウント
  - テナントスイッチャー（所属を選択）
  
- **前回のセッションを続行する**
- **これらのプロントブックの使用を開始する**
  - 使用可能なプロンプトブックのサブセットのカードを表示
  - タイトルクリックで詳細ページを開く（ここから新たなセッションを開始可能）
- **プロンプトバー**
  - 会話の開始に使用
  - プロンプトブックとシステム機能を検索してアクセスする機能付き（別ウィンドウ）
    - プロンプトバー内のプロンプトアイコンをクリックすると開ける
- **ヘルプ**

#### セッションで利用できる機能
- プロセスログ
  - Copilotが応答を生成する過程を表示
  - 生成に使用される機能やデータのソースを確認できる
  ![image](https://github.com/user-attachments/assets/1672b918-9510-4171-beaf-70b6971b62ab)

- プロンプトに対するフィードバック
  - 選択できるオプションは次の通り
    - 適切（Looks right)
    - 改善が必要 (Needs improvement)
    - 不適切 (Inappropriate）
  - 各オプションについて、追加情報の入力ができる
  ![image](https://github.com/user-attachments/assets/6f677d8a-bab7-42e6-9766-1353df2457bc)

- ピンボード
  - 個別または複数のプロンプトと応答のペアをピン留め
  - 内容を、Copilotへのアクセス権を持つ組織内のユーザに共有可
  - Microsoft Word へエクスポート可
  - メールで送信可
  - コピー可

### 利用できるMicrosoftプラグイン（抜粋）
#### Microsoft Entra
- ID（アカウント）とネットワークアクセスの管理用の統合プラットフォーム
#### Microsoft Defender XDR
- 関連するプラグイン
  - Microsoft Defender XDR
  - Microsoft Defender XDR 用 Natural Language to KQL
- "Microsoft Defender XDR"
  - 詳細は[こちら](Microsoft_Defender_XDR.md)
- "Microsoft Defender XDR 用 Natural Language to KQL"
  - 自然言語による質問を KQL クエリに変換できるクエリアシスタント機能
    
#### Microsoft Defender External Attack Surface Management（Defender EASM）
- Attack Surface：サイバー攻撃を試みることができるすべてのポイントや経路（攻撃対象領域）
- ITインフラを監視し、外部に露出している攻撃対象となり得る領域を検出して可視化する
- サポートされている機能（抜粋）
  - Attack Surface の概要の取得
  - Attack Surface の分析情報を取得
  - 優先度または CVE ID によって CVE の影響を受ける資産を取得する
  - 脆弱性の重大度とリスクで示す CVSS スコアを用いて（影響を受ける）資産を取得する
  - 期限切れのドメインや SSL 証明書を取得する　など
- 利用のためにサブスクリプションが必要（詳細は[こちら](https://learn.microsoft.com/ja-jp/azure/external-attack-surface-management/easm-copilot))
  
#### Microsoft Defender 脅威インテリジェンス（Defender TI）
- 脅威インフラストラクチャの分析と脅威インテリジェンスの収集を行うときのワークフローを合理化するプラットフォーム
- このプラグインにより提供される情報
  - 脅威アクティビティグループ
  - 侵害インジケーター(IOC)
  - ツール
  - コンテキストに対応した脅威インテリジェンス

### サポートされているMicrosoft以外のプラグイン
#### 3つに分類
- その他
  - Splunkなど
  - 利用には、特定のサービスに対するアカウントとライセンス、および認証を含むセットアップが必要
- Webサイト
- カスタム
  - 種類
    - 独自開発の Copilot プラグイン
    - OpanAI APIを用いて開発した Copilot プラグイン
  - スキルセットに関するメタデータとスキルの呼び出し方法を記述するYAMLまたはJSON形式のマニフェストファイル(plugin.yaml や plugin.json など)が必要
  - 使用権限のカスタマイズが可能（詳細は[こちら](https://learn.microsoft.com/ja-jp/copilot/security/manage-plugins?tabs=securitycopilotplugin))
  
