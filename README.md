# Animals

## Asset
https://assetstore.unity.com/packages/3d/characters/animals/lovely-animals-pack-92629

## アクセサリーとしてアップロードを試す
1. からのオブジェクトを作成し、その中に元々あったプレハブを入れる
2. それ自体をプレハブにする（ドラッグ&ドロップ）
3. アップロードしようとすると以下のエラー
  * アニメーション使えないよ
    * アニメーションは普通に剥がした（紐づいていたアニメーションのコンポーネントを削除）
  * MeshRendererしかサポートしてないよ
    * SkinnedMeshBakerというツールでMeshRendererに変換して、SkinnedMeshRendererがついていたコンポーネントを削除した