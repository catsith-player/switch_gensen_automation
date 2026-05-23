# Switch厳選自動化ツール
## ツールについて
Rasberry Pi Picoを使用してNintendo Switch/Switch2の厳選処理(主にポケモンレジェンズ)を自動化するWindowsアプリです。

以下の機能を実装しています。
* ZA ドーナツ厳選 自動化
* マクロコントローラとしての使用

ツールの使用にあたり、必要なものは以下の通りです。
- Windows 10/11 64bitのPC
    - Core i5 / Ryzen 5 以上
    - メモリ 8GB以上
- Rasberry pi pico
- USBシリアル変換アダプタ
- ジャンパワイヤー
- キャプチャーボード
  - ZA ドーナツ厳選 自動化を行う場合
- 各種ケーブル


## ダウンロード
[releaseページ](https://github.com/catsith-player/switch_gensen_automation/releases)よりzipファイルをダウンロードしてください。

## 起動方法

展開したフォルダ内の `SwitchSelectionAutomator.bat` を起動してください。  

アプリ本体と DLL 類は `app` フォルダにまとめています。  
設定ファイルは `app\settings` フォルダに保存されます。

## 更新時の注意

新しいバージョンへ更新するときは、必要に応じて既存の `app\settings` フォルダを引き継いでください。

### 更新履歴

| バージョン | 日時 | 備考 |
| --- | --- | --- |
| 0.1.0 | 2026/5/23 | 初期バージョンの公開 |

## 同梱物とライセンスについて

この配布物には、アプリ本体の動作に必要なランタイム、ライブラリ、データ、Pico 用ファームウェアを同梱しています。

| 同梱物 | 用途 | ライセンス・確認先 |
| --- | --- | --- |
| .NET runtime files | self-contained publish により同梱 | 主に MIT License / <https://github.com/dotnet/runtime> |
| OpenCvSharp / OpenCV runtime | キャプチャ画像処理 | OpenCvSharp: BSD 3-Clause License / <https://github.com/shimat/opencvsharp><br>OpenCV: Apache License 2.0 系 / <https://github.com/opencv/opencv> |
| Tesseract OCR | 文字認識 | Apache License 2.0 系 / <https://github.com/tesseract-ocr/tesseract><br>.NET wrapper: <https://github.com/charlesw/tesseract> |
| `jpn.traineddata` | 日本語 OCR 用の学習データ | Apache License 2.0 系 / <https://github.com/tesseract-ocr/tessdata> |
| Pico firmware UF2 | Pico を Switch 用コントローラとして動作させるファームウェア | `app\Firmware\pico-switch-controller.uf2` として同梱 |
| touchgadget/switch_tinyusb | Pico firmware 内の Switch HID descriptor / report 形状の参考 | MIT License / <https://github.com/touchgadget/switch_tinyusb> |
| Adafruit TinyUSB Library | Pico firmware のビルドに使用 | <https://github.com/adafruit/Adafruit_TinyUSB_Arduino> |

公開配布する場合は、使用している各 OSS のライセンス本文、著作権表示、再配布条件を確認してください。
