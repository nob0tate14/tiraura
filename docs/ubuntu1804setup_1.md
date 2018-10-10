VirtualBoxにubuntu18.04LTSを追加したメモ

環境：Windows10のVirtualBoxのUbuntu18.04LTS

チップセット：ICH9  
PAE/NX：有効  
準仮想化インターフェース：KVM  
仮想化支援機能：両方有効化  
ストレージ：可変サイズ、20Gくらい、、、10Gだとすぐいっぱいになる  

UJTから物をいただく  
最小インストール  

16.04LTSはappstreamの問題が発生して手こずった。  
17はすぐに捨てた。  
18は概ね調子よい  

GuestAdditionsをインストール  

sudo apt update  
ひとしきり更新して最新のOS状態にする。  
