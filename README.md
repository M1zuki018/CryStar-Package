# CryStar Custom Attributes

Unity向けのカスタム属性とPropertyDrawerコレクション。インスペクターの使いやすさを大幅に向上させる便利な属性を提供します。

## 特徴

- **CommentAttribute**: 変数名を日本語コメントに置き換え
- **ExpandableSOAttribute**: ScriptableObjectをインスペクター上で直接編集
- **HighlightIfNullAttribute**: 未割り当て参照を赤色でハイライト
- **MethodButtonInspectorAttribute**: インスペクターにメソッド実行ボタンを追加
- **TagSelectorAttribute**: タグをプルダウンから選択可能に

## インストール

### Package Manager経由（推奨）

1. Unity Package Managerを開く
2. `+` → `Add package from git URL...`
3. 以下のURLを入力：

```
https://github.com/M1zuki018/crystar-custom-attributes.git
```

### 特定のバージョンをインストール

```
https://github.com/M1zuki018/crystar-custom-attributes.git#v1.0.0
```

### manifest.jsonに直接追加

`Packages/manifest.json`に以下を追加：

```json
{
  "dependencies": {
    "com.crystar.custom-attributes": "https://github.com/M1zuki018/crystar-custom-attributes.git"
  }
}
```

## 使用方法

### CommentAttribute

変数名を日本語コメントに置き換えます：

```csharp
using CryStar.Attribute;

public class Player : MonoBehaviour
{
    [SerializeField, Comment("プレイヤーの最大体力")]
    private int _maxHealth = 100;
    
    [SerializeField, Comment("移動速度（m/s）")]
    private float _moveSpeed = 5.0f;
}
```

### ExpandableSOAttribute

ScriptableObjectをインスペクター上で直接編集できます：

```csharp
[SerializeField, ExpandableSO]
private GameSettings _gameSettings;

[SerializeField, ExpandableSO(defaultExpanded: false, useBackground: false)]
private AudioSettings _audioSettings;
```

### HighlightIfNullAttribute

未割り当ての参照を赤色でハイライトします：

```csharp
[SerializeField, HighlightIfNull]
private GameObject _targetObject;

[SerializeField, HighlightIfNull]
private Transform _spawnPoint;
```

### MethodButtonInspectorAttribute

インスペクターにメソッド実行ボタンを追加します：

```csharp
[MethodButtonInspector("体力を回復")]
private void RestoreHealth()
{
    // 体力回復処理
}

[MethodButtonInspector()] // メソッド名をボタンラベルとして使用
private void ResetSettings()
{
    // 設定リセット処理
}
```

### TagSelectorAttribute

タグをプルダウンから選択できます：

```csharp
[SerializeField, TagSelector]
private string _enemyTag = "Enemy";
```

## 要件

- Unity 2022.3 以上
- .NET Standard 2.1

## ライセンス

MIT License

## サポート

Issue報告やフィードバックは[GitHubリポジトリ](https://github.com/M1zuki018/crystar-custom-attributes)までお願いします。

## 変更履歴

詳細な変更履歴は[CHANGELOG.md](CHANGELOG.md)をご覧ください。
