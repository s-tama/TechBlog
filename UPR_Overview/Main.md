# URPを覚えよう UniversalRenderPiplineAsset
# URPを覚えよう ～特徴からプロジェクト作成まで～

この記事はURPを勉強し始めた筆者のメモ書きです

<details open>
<summary>目次</summary>

ついにこの時が...
1. Universal Render Pipline ( URP ) って何？
2. Scriptable Render Pipline ( SRP ) について
3. URPの使用方法
4. URPテンプレートについて

</details>

## ついにこの時が...
現在開発中のゲームでURPを使用することになりました。  
実は前々から興味はあれど手をつけずにいたので、この機会にちゃんと勉強します。

## 1.Universal Render Pipline ( URP ) とは
Unity2021を目途に完全にBuilt-inに代わるレンダーパイプラインとして使用されるパイプラインです。
URPはオープンソースとなっており、現在も[GitHub](https://github.com/Unity-Technologies/Graphics)にて開発が進められています。

- Universal Render Pipline、通称URPは、UnityデフォルトのパイプラインであるBuilt-in Render Piplineの後継として採用されることが決まっている新しいパイプラインの事
- 今まではLighht Weight Render Pipline、通称LWRPとして配布されていたが、unity2018以降、URPに改名

## 2. Scriptable Render Pipline ( SRP ) について
Unity公式マニュアルの説明です  
https://docs.unity3d.com/ja/2018.4/Manual/ScriptableRenderPipeline.html  

公式の説明によると、完全にカスタマイズ可能なパイプラインとなっています。

SRP自体は「Package Manager」または開発中のGitHubからインポートすることで使用可能
Packagemanagerからインポート
<!-- ここにPackageManagerからのインポート方法の画像を記載 -->
GitHubからインポート
<!-- ここにGitHubからのインポート方法の画像を記載 -->

## URPの特徴
- URPはモバイルからハイエンドなコンソールゲームまで、幅広い表現を可能としている
- 「シングルパス・フォワードレンダリング」というレンダリング方式を採用しており、ドローコール数を抑える事が可能
- カメラごとに「2D」「3D」のレンダラーを分けて使用することが可能（それぞれ実行されるパスが異なる）
    - Forward Renderer : シングルパス・フォワードレンダリング
    - 2D Renderer : 2D専用のレンダリング（この機能はURPのみに採用されている）
    - Custom Renderer : 独自にカスタムしたレンダラーに切り替えることも可能

## URPで使用できるシェーダ
URPではビルトインに変わる標準シェーダとして以下が提供用意されています
- Lit : 物理ベースのシェーダ
- Simple Lit : 非物理ベースのシェーダ
- Baked Lit : 動的なライティングを行わないシェーダ

ビルトインから用意されているシェーダでは、以下が使用可能となっています
- Unlit : ライトの影響を受けないシェーダ

## Built inとURP

## 3.URPの使用方法


## 4.URPテンプレート