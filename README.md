# flutter_unity_widget_sample01
A new Flutter project.

# 環境ビルド手順

## clune して Pods などの更新をする
```
git clone git@github.com:tfuru/flutter_unity_widget_sample01.git
cd flutter_unity_widget_sample01
```

## Unity で Flutter プロジェクトをビルド
1. Unityで `unity/sample01` を開く
2. `Asset/Scenes/SampleScene` を開く
3. メニュー Flutter -> Export iOS を選択して出力
`ios/UnityLibrary` が生成されるはず

## Xcode で ビルド設定 
1. ワークスペースを開く
```
cd flutter_unity_widget_sample01

# 不要ファイルを削除
flutter pub remove flutter_unity_widget
flutter pub add flutter_unity_widget
flutter clean

# ビルド失敗するが flutter 関連 Pods プロジェクトが生成される
flutter build ios

open ios/Runner.xcworkspace/
```

2. `Unity-iPhone`, `Runner`, `Pods` の ３つのワークスペースが表示されているはず
3. Teams 設定の確認
4. ビルドを試す 
