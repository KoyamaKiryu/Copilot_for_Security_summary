# Microsoft Defender XDR
- エンドポイント、アプリケーション、メール、ID からの脅威シグナルを評価して、攻撃の範囲と影響を特定可能
- 攻撃を防止または停止するための自動アクションを実行可能
-  Microsoft Defender 脅威インテリジェンスへのアクセス（サブスクリプション）

## 保護対象と保護を行うための仕組み
- [Microsoft Defender for Endpoint](https://github.com/KoyamaKiryu/Copilot_for_Security_summary/edit/main/jp/Microsoft_Defender_XDR.md#microsoft-defender-for-endpoint) によるエンドポイントの保護
- [Microsoft Defender Vulnerability Management](https://github.com/KoyamaKiryu/Copilot_for_Security_summary/edit/main/jp/Microsoft_Defender_XDR.md#microsoft-defender-vulnerability-management) による資産の保護
- [Microsoft Defender for office 365](https://github.com/KoyamaKiryu/Copilot_for_Security_summary/edit/main/jp/Microsoft_Defender_XDR.md#microsoft-defender-for-office-365) によるEmailとコラボレーションツールの保護
- [Microsoft Defender for Identity](https://github.com/KoyamaKiryu/Copilot_for_Security_summary/edit/main/jp/Microsoft_Defender_XDR.md#microsoft-defender-for-identity) によるIDの保護
- [Microsoft Defender for Cloud Apps](https://github.com/KoyamaKiryu/Copilot_for_Security_summary/edit/main/jp/Microsoft_Defender_XDR.md#microsoft-copilot-for-cloud-apps) によるアプリケーションの保護

### Microsoft Defender for Endpoint
- エンドポイントを企業ネットワークが保護できるように設計されたプラットフォーム

#### 提供機能
- Core Defender Vulnerbility Management （組み込み型の脆弱性管理機能）
- アタックサーフェイスの削減
- 次世代の保護機能（新しい脅威に対する保護機能）
  - 振る舞いベース、ヒューリスティックでリアルタイムのアンチウィルス保護
  - クラウドベースの保護機能
  - 新たな脅威に特化した保護機能と製品の更新
- エンドポイントにおける検知と対応
- 調査と修復の自動化（AIR）
- Microsoft Secure Score for Devices
  - 企業ネットワークの動的に評価し、保護されていないシステムの特定が可能
  - 全体的なセキュリティを強化するために推奨されるアクションの実行を支援
- Microsoft Threat Experts（脅威ハンティングサービスを管理）
- 操作とAPI
  - 標準の Microsoft Entra ID ベースの認証と認可モデルを介してエンティティと機能を公開するように設計された API モデルを提供


### Microsoft Defender Vulnerability Management
- 資産の可視化
- Windows、macOS、Linux、Android、iOS、ネットワーク デバイス用の修復ツールを提供
- 速くかつ継続的に重要な資産が保持する脆弱性について優先順位を付け、リスクを軽減するための推奨事項を提供
  ![image](https://github.com/user-attachments/assets/6ee7ae9b-6897-4a75-a1d9-371cb08065fa)
- ダッシュボード
  ![image](https://github.com/user-attachments/assets/3ac3b1c7-0370-40bd-bc6d-02b4ad459378)


### Microsoft Defender for office 365
- office 365 のサブスクリプションに含まれている
- メールやコラボレーション ツール(SharePoint、Teams、Outlook など)で届くフィッシングやマルウェアなどの脅威からの保護機能
- 脅威のリアルタイム表示
- インシデントレスポンスを支援するための調査、ハンティング、修復機能

#### 提供機能
- 事前設定済みのセキュリティポリシー
- 脅威保護ポリシー
- リアルタイムレポート
- 脅威の調査と対応機能
- 脅威の調査と対応の自動化機能


### Microsoft Defender for Identity
- クラウドベースのセキュリティソリューション
- 組織を対象とする高度な脅威、侵害された ID、および悪意のある内部関係者によるアクションが特定、検出、調査

#### 提供機能
- ユーザの振る舞いとアクティビティの監視
- Active Directory内のユーザIDと資格情報の保護
- サイバーキルチェーン全体にわたって、疑わしいアクティビティや高度な攻撃を特定する
  - 偵察
  - 侵害された資格情報
  - 横方向の移動
  - ドメインの支配
- アラートとユーザアクティビティの調査
  ![image](https://github.com/user-attachments/assets/bbf90b5f-fab8-473a-ba05-7cb0518fecdf)


### Microsoft Defender for Cloud Apps
- SaaSアプリケーションの保護
- クラウドアプリデータの監視・保護支援

#### 提供機能
- SaaSアプリケーションの検出
  - 識別：各ユーザがアクセスするアプリを識別
  - 評価：検出されたアプリを90以上の指標でリスク評価
  - 管理：アプリを常時監視するポリシーの設定、異常検知によるアラートの送信
- 情報の保護
  - 秘密度ラベルの設定
  - 管理していないデバイスへのダウンロードのブロック
  - 機密ファイルのアクセス者リストから部外者を外す
- SaaS Security Posture Management (SSPM)
- 高度な脅威保護
  - 組み込みの適応型アクセス制御 (AAC)
  - ユーザーとエンティティの動作分析 (UEBA)
- アプリガバナンス関連の機能を用いたアプリ間通信保護
  ![image](https://github.com/user-attachments/assets/d665712b-d171-4f35-84e9-e049fd538aae)

# Microsoft Copilot for Microsoft Defender XDR
- インシデントを迅速かつ効率的に調査するツール
- Microsoft Copilot for security 埋め込みエクスペリエンス
- 他のMicrosoft製品等も利用したより詳細な調査をする際は、スタンドアロン エクスペリエンスに移行

## サポートする機能（概要は[こちら](https://learn.microsoft.com/ja-jp/training/modules/security-copilot-embedded-experiences/2-copilot-for-defender))
- インシデントの要約
- 対応手続きに関するガイド付きの応答
- スクリプトとコードの分析
- 自然言語よるKQLクエリの生成
- インシデントレポートの作成
- ファイルの分析
- デバイスの概要情報の取得
- 生成結果に対するフィードバックの提供
- スタンドアロン エクスペリエンスへの移行
