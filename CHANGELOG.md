# Changelog

## [v0.1.1] - 2024-03-XX

### 追加
- ベンチマーク機能の強化
  - 2準位系と調和振動子のベンチマーク追加
  - Python/C++実装の詳細な性能比較機能
  - プロファイリング機能（CPU使用率、メモリ使用量、スレッド数など）
- 新しい例題の追加
  - 2準位系の励起ダイナミクスシミュレーション
  - 調和振動子のダイナミクスシミュレーション
  - 解析解との比較機能

### 改善
- 性能最適化
  - 疎行列パターンの再利用による行列更新の高速化
  - OpenMP並列化の改善（動的スケジューリング、チャンクサイズの最適化）
  - メモリアライメントの最適化（キャッシュライン境界の考慮）
- ベンチマーク結果の可視化
  - 実行時間、CPU使用率、メモリ使用量などの詳細なプロット
  - Python/C++実装の性能比較グラフ
  - 行列サイズに対するスケーリング特性の分析

### ドキュメント
- プロファイリング結果のレポート追加
- ベンチマーク手順と結果の詳細な説明
- 例題の理論背景と実装の解説

## [v0.1.0] - 2024-07-07

### 追加
- Python実装からC++への移行完了
- OpenMPによる並列化サポート
- ベンチマーク機能の実装
- 二準位系のテストケース実装

### パフォーマンス
- 行列更新時間: 0.007-0.074ms
- RK4ステップ時間: 0.013-0.204ms
- Python実装との比較: 0.7-0.8倍（現時点では若干遅い）

### 検証済み機能
- CSR形式の疎行列サポート
- 時間発展の数値的安定性
- Python/C++実装間の結果一致（差: 10^-15オーダー）
- 解析解との一致（差: 約2.7%）

### 既知の課題
- Python実装より若干遅い実行速度
- データ変換のオーバーヘッド
- 小規模行列での非効率性

### 今後の改善点
- データ変換の最適化
- メモリ管理の改善
- OpenMP設定の最適化
- 大規模行列での性能評価 