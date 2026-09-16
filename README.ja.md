### ![en](https://flagcdn.com/20x15/gb.png) [English Here](README.md)

# ssbu-snappy-syncer

大乱闘スマッシュブラザーズ SPECIALの操作遅延を4F削るMod．他の低遅延Modと役割は同じですが，[ssbu-online-deluxe](https://github.com/saad-script/ssbu-online-deluxe)と同じく最大の遅延を安定して削ることができ，対戦相手や他人に情報が表示されないためModの有無が分かりにくいです．

[ssbu-combat-latency-slider](https://github.com/Atamol/ssbu-combat-latency-slider)とは同時に使用可能ですが，[ssbu-vsync-disabler](https://github.com/Atamol/ssbu-vsync-disabler)とは競合します．

> v13.0.5専用です．自己責任で使用してください，知らんけど．

## 機能・特徴

* シンプル

他のプラグインに依存しません．

* オーバークロック，解像度の制限

13.0.4までは素のクロックで-4Fの低遅延を維持できましたが，13.0.5では不可能なためクロックを調整しています．

また，1080p (FHD) ではなく720pで動作するようになっており，configから1080pへの変更もできますが，一部シーンでラグが起きる可能性があります．どうしても気になる方は，[ssbu-combat-latency-slider](https://github.com/Atamol/ssbu-combat-latency-slider) + [ssbu-vsync-disabler](https://github.com/Atamol/ssbu-vsync-disabler)の組み合わせも試してみてください．

* 重いHS，重い撃墜演出，手前撃墜の不具合の修正

重いヒットストップ，重い撃墜演出，手前撃墜の時に起こるラグがありません (OC有効時)．

## インストール

1. [Release](https://github.com/Atamol/ssbu-snappy-syncer/releases)から最新の`atmosphere`フォルダをSDカードのルートにコピー
2. 本体を再起動 (アルバム → Reboot to Payload)

## 設定

初回起動時に `sd:/ultimate/ssbu-snappy-syncer/config.txt` が生成されます．

**原則として，デフォルトのまま使用してください**．

| キー                     | デフォルト         |                                                                                              |
| ------------------------ | ------------------ | -------------------------------------------------------------------------------------------- |
| `index_mode`           | `0`              | 0: 最低遅延，1: +1F，2: バニラ                                                               |
| `render_opts`          | `true`           | ファイターの描画コマンドをシーン更新の後に記録する                                           |
| `double_buffer`        | `true`           | `false`: トリプルバッファ                                                                  |
| `resolution`           | `720p`           | 1080p では描画が重くなり，576p はキャラのカットインやカウントダウンなどの表示が欠ける        |
| `vsync`                | `false`          |                                                                                              |
| `pacer`                | `true`           |                                                                                              |
| `cutin_render_opts`    | `true`           | 撃墜演出の間だけ描画最適化を切る                                                             |
| `match_only_immediate` | `true`           |                                                                                              |
| `overclock`            | `true`           |                                                                                              |
| `overclock_by_match`   | `true`           |                                                                                              |
| `overclock_profile`    | auto               | `singles`: 1428，`ffa`: 1683，auto: 人数で自動選択 (3人乱闘以上になるとクロックが上がる) |
| `overclock_custom`     | `1785,1267,1996` | `cpu,gpu,mem` をMHzで指定する．ドックに挿した状態のみ                                      |
| `legacy_sync`          | `false`          |                                                                                              |
