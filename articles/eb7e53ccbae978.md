---
title: "Yubikeyに設定したOpenPGPの情報を消す方法"
emoji: "🔓"
type: "tech" # tech: 技術記事 / idea: アイデア
topics: ["YubiKey","OpenPGP","PGP"]
published: false
---
# この記事の目的
私のようにYubikeyに設定したPGP関連のPINを忘れて何もできなくなってしまった方向けの記事です。  
Yubikeyに設定されたOpenPGPの情報のリセットを行います。  

# 環境
今回はWindowsで行いましたがMacOSやLinuxでも似たような手順で行えるかと思います。  
YubikeyManagerをインストールされていない方はインストールしてください。  
https://www.yubico.com/support/download/yubikey-manager/

# 手順
PowerShellなどのターミナルを開いて、リセットしたいYubikeyを挿入してください。  

次にYubikeyManagerのインストールディレクトリに移動してください。  
```
cd "C:\hoge\...\Yubikey Manager"
```
ここで
```
./ykman.exe openpgp reset
```
を実行することでOpenPGPの情報が消え、新しい鍵を設定することができるようになります。  

:::message alert
再設定するときはPINを忘れないようにどこかにメモしておきましょう。
:::
# 最後に
この記事をご覧いただきありがとうございます。  
少しでもみなさんのお役に立てたのなら幸いです。  
そうでなければごめんなさい。  
ほかはGUIからリセットかけられるのになんでPGPだけできないんだろう......

# 参考文献
https://support.yubico.com/hc/en-us/articles/360013761339-Resetting-the-OpenPGP-Application-on-the-YubiKey