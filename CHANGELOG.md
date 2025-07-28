# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [1.0.0] - 2025-07-28

### Added
- **CommentAttribute**: 変数名を日本語コメントに置き換える属性
- **ExpandableSOAttribute**: ScriptableObjectをインスペクター上で直接編集可能にする属性
- **HighlightIfNullAttribute**: 未割り当て参照を赤色でハイライトする属性
- **MethodButtonInspectorAttribute**: インスペクターにメソッド実行ボタンを追加する属性
- **TagSelectorAttribute**: タグをプルダウンから選択可能にする属性
- **AudioType**: オーディオ種別の列挙型（Master, BGM, SE, Ambience, Voice）
- **LanguageType**: 言語種別の列挙型（Japanese, English）
- **ServiceType**: サービスロケーター登録種別の列挙型（Global, Local）

### Features
- Unity 2022.3以上をサポート
- Assembly Definition Filesによる適切な依存関係管理
- 包括的なサンプルコードとドキュメント
- PropertyDrawerの最適化とパフォーマンス向上
- エラーハンドリングとメモリリーク防止

### Documentation
- 詳細な使用例とAPI仕様
- インストール手順の完備
- ベストプラクティスガイド

### Performance
- SerializedObjectキャッシュによるExpandableSODrawerの最適化
- リフレクションキャッシュによるMethodButtonInspectorDrawerの高速化