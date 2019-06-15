# 動画配信を試してみる

nginx + なにかをつかって映像配信

## 実験サーバのスペック

- 回線: 1Gbps
- CPU: Xeon E3-1235L v5
- RAM: DDR4 16GB ECC
- NIC: 1GbE x2
- メイン: SSD 256GB + HDD 1TB
- データ: HDD 4TB x2

## 検討中

調べ次第追記

- HLS
  - pros
    - 楽そう(有効化だけならモジュール読み込み => `hls on` だけでほぼOK)
    - ユーザの回線状況に応じたビットレート選択
  - cons
    - コーデック依存(mp4 => ts, m3u8 に分割)
    - 小さなファイルを断片的に送るのでHDDだときびつい(気がする)
- WebRTC
  - pros
    - 低遅延
    - ユーザの回線状況に応じたビットレート選択
  - cons
    - コーデック依存
- MPEG-DASH
  - pros
    - コーデック依存なし <= 過去の資産が活かせるので爆アド
  - cons
- progressive download
  - pros
  - cons
    - コーデック依存