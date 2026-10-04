# human-friendly-gui-skills

操作導線、情報の圧縮、アフォーダンス、冗長性、認知負荷を作業目的から判断する、設計とレビューの2つのGUIスキルです。

ブラウザとデスクトップの両方に適用でき、特定のフレームワークを前提にしません。共通原則を中心に、実行環境に固有の確認事項を対象の作業に応じて選びます。単一HTMLのモックは設計確認用の標準であり、本番アプリの技術や構成を制約しません。

- [設計スキル](.agents/skills/human-friendly-gui-design/SKILL.md): 新規設計、既存画面の改善案の具体化・実装、HTMLモック作成
- [レビュースキル](.agents/skills/human-friendly-gui-review/SKILL.md): 既存画面や画面案の問題点、改善の方向性、優先度の評価
- [HTMLモックの作り方](.agents/skills/human-friendly-gui-design/references/html-mockups.md)
- [レビュー観点](.agents/skills/human-friendly-gui-review/references/review-checklist.md)
- [テンプレートの選択基準](.agents/skills/human-friendly-gui-design/references/template-selection.md)
- [ホーム・モード切替の判断基準](.agents/skills/human-friendly-gui-design/references/app-navigation.md)
- [表示・操作・実行方式の判断基準](.agents/skills/human-friendly-gui-design/references/interaction-patterns.md)
- [テンプレート一覧HTML](mockups/template-catalog.html): ナビゲーション2種類、作業画面8種類と取り込み設定付きの派生を開いて比較できます
- [モックHTMLの配置先](mockups/)

## 利用方法

画面案を具体化するときは `$human-friendly-gui-design`、問題点と優先度を評価するときは `$human-friendly-gui-review` を指定します。

依頼では対象の作業や画面と、求める範囲を伝えます。設計には「新しい画面のHTMLモックを作成」「既存画面の機能を保って改善」、レビューには「画面の問題点だけレビュー」のように指定できます。レビューと改善の両方を依頼した場合は、範囲内で両方を使えます。

他のリポジトリで使う場合は、必要なスキルのフォルダを `.agents/skills/` へ配置してください。各スキルは、同梱の参照資料だけで単独利用できます。設計側の自己検証とレビュー側の評価で使う `references/review-checklist.md` は同内容を同梱しています。共通観点を変更するときは両方を更新してください。

`mockups/` は、このリポジトリで作るモックHTMLの保存先です。他のリポジトリでの出力先は利用者の指定や既存の文書配置を優先します。

ホームは独立した作業の開始、サイドパネルは関連モード間の往復に使います。実行・ジョブ管理ではカード／表、逐次／並列、比較画面では同一画面／専用画面をモック上で切り替えて検討できます。本番の構成は作業と処理負荷に合わせて選び、モックの比較用スイッチをそのまま実装要件にしません。
