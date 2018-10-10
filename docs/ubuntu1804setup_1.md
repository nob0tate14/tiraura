VirtualBoxにubuntu18.04LTSを追加するメモ

環境：Windows10のVirtualBoxのUbuntu18.04LTS

チップセット：ICH9  
PAE/NX：有効  
準仮想化インターフェース：KVM  
仮想化支援機能：両方有効化  
ストレージ：可変サイズ、20Gくらい10Gだとすぐいっぱいになる  

UJTから物をいただく  
最小インストール  

16.04LTSはappstreamの問題が発生して手こずった。  
17はすぐに捨てた。  
18は概ね調子よい  

GuestAdditionsをインストール  

Pythonは3.6.5が入っていた。

sudo apt update  
ひとしきり更新して最新のOS状態にする。  
