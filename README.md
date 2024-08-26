# Cluster Accessories

## Asset
https://assetstore.unity.com/packages/3d/characters/animals/lovely-animals-pack-92629

## アクセサリーとしてアップロードを試す
1. からのオブジェクトを作成し、その中に元々あったプレハブを入れる
2. それ自体をプレハブにする（ドラッグ&ドロップ）
3. アップロードしようとすると以下のエラー
  * `ArgumentException: Value does not fall within the expected range.`
    * プレハブにItemコンポーネントが紐づいていなかった
    * 紐づいけて再度アップロードしても失敗した
    * 再度プレハブを作り直し（ドラッグ&ドロップし直し）たら上手く行った
  * アニメーション使えないよ
    * アニメーションは普通に剥がした（紐づいていたアニメーションのコンポーネントを削除）
  * MeshRendererしかサポートしてないよ
    * SkinnedMeshBakerというツールでMeshRendererに変換して、SkinnedMeshRendererがついていたコンポーネントを削除した
  * (別件)AssetのVRM内にあるMToonと、Clusterクリエーターキットに入っているMToonが競合することによりエラー
    * Clusterクリエイターキットの方がReadOnlyになっていたのでVRMの中のMToonを削除
    * ピンク色になったやつは別のシェーダーが選択されていたので、改めてMToonを付け直し
