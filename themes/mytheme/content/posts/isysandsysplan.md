+++
title = '情報システム戦略とシステム企画'
date = 2024-02-23T15:16:32+09:00
draft = false
isCJKLanguage = true
tags = ['応用情報技術者試験','ストラテジ']
[params]
    subtitle = '応用情報技術者試験'
+++

##### 目次
1. 全体最適化計画とシステム化計画
2. エンタープライズアーキテクチャ(EA)
3. 要求分析・要件定義・調達

#### 全体最適化計画とシステム化計画
* 全体最適化計画は業務とシステムが進むべき方向を示すこと
* システム化計画は全体最適化計画を基に計画を立案

**全体最適化計画**:組織全体として業務とシステムが進むべき方向を示す計画で、全体最適化目標、ITガバナンス[^1]の方向、経営戦略との整合性、情報システムのあるべき姿(To-beモデル)などが検討される

**システム化計画**:全体最適化計画に基づき、各部門において個別に作られたルールや情報システムを統合化し、効率性や有効性を向上させるための計画

##### ビジネスモデルとビジネスプロセス
* **ビジネスモデル**:ビジネスコンセプトを具体化させるための枠組みで、利益を生み出すビジネスの手順の雛形
* **ビジネスプロセス**:業務の流れを細分化したもの

##### 業務モデル
情報システムの全体計画の土台になるもので、業務を抽象化して表現したものである。
UMLやDFD、E-Rダイアグラムなどが使われる。

##### 情報システムモデル
ここのビジネスプロセス間の連携を円滑にするための情報システム群。インターネット受注システムやクレジット会社との連携が該当する。

#### エンタープライズアーキテクチャ(EA)
* EAは組織全体の最適化を実現するための概念
* EAの構成要素にはBA、DA、AA、TAがある。

##### EAの構成要素
EAを構成する要素は、ビジネスアーキテクチャ、データアーキテクチャ、アプリケーションアーキテクチャ、テクノロジアーキテクチャがある。
* **ビジネスアキテクチャ**:組織の目標や業務を体系化したアーキテクチャ
* **データアキテクチャ**:組織の目標や業務に必要となるデータの構成、データ間の連携を体系化したアーキテクチャ
* **アプリケーションアーキテクチャ**:組織の目標を実現するために業務と、それを実現するアプリケーションの関係を体系化したアーキテクチャ
* **テクノロジアーキテクチャ**:業務を実現するためのハードウェア、ソフトウェア、ネットワークの技術を体系化したアーキテクチャ

#### 要求分析・要件定義・調達
* 要件定義には業務要件定義、機能要件定義、非機能要件定義がある
* ファブレスは生産設備をもたず外部に生産を委託

**要求分析**は新たなシステムやシステム更新に際しての調査、定義に関わる工程である要求項目を洗い出し、分析、システム化、ニーズの整理、前提条件や制約事項の整理という手順で行われる。

**要件定義**はシステムやソフトウェア開発において実装するべき機能や満たすべき性能などを明確にしていく作業

##### RFPとRFI
* **RFP**[^2]:受注側がベンダー企業に提案書の提出を依頼するための文書
* **RFI**[^3]:ベンダー企業に対しシステム化の目的や業務概要を明示し、情報提供を依頼すること

##### 要件定義
* **機能要件定義**:業務要件を実現するために必要な情報システムの機能を明らかにする
* **非機能要件定義**:パフォーマンスや信頼性(品質)、移行要件など 


[^1]: ITガバナンス:企業が競争優位性の構築を目的にIT戦略の策定・実行を統制し、あるべき方向を導く組織能力
[^2]: RFP(Request For Proposal:提案依頼書)
[^3]: RFI(Request For Information:情報提供依頼)