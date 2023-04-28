---
lab:
  title: ラボ 2:キャンバス アプリをビルドする方法
  module: 'Module 3: Get started with Power Apps'
ms.openlocfilehash: 9a9a447ac07176e7f7ed3471c105b2d06fa60c97
ms.sourcegitcommit: 8a89b7eacd1a65eaa7c5d6bff0dc7254991c4dde
ms.translationtype: HT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/15/2022
ms.locfileid: "147154433"
---
# <a name="lab-2-how-to-build-a-canvas-app"></a>ラボ 2:キャンバス アプリをビルドする方法

## <a name="scenario"></a>シナリオ

ベローズ カレッジは、キャンパス内に複数の建物を持つ教育機関です。 キャンパス訪問は現在、紙の記録簿に記録されています。 その情報は一貫して把握されておらず、キャンパス全体の訪問に関するデータを収集して分析する手段もありません。

現在、キャンパス管理では、Excel スプレッドシートを利用して訪問者の登録を追跡しています。 現在の訪問者登録システムでは、建物へのアクセスがセキュリティ担当者によって管理されており、すべての訪問を訪問先で事前に登録し、記録する必要があるため、カレッジではこのシステムを最新化したいと考えています。

このコース全体を通して、アプリケーションを構築するとともに自動化を行って、ベローズ カレッジの管理担当者とセキュリティ担当者がキャンパス内の建物へのアクセスを管理および制御できるようにします。

## <a name="high-level-lab-steps"></a>ラボ手順の概要

キャンバス アプリを設計するには、以下の概要に従います。

- 訪問テーブルのデータからキャンバス アプリを作成する

- 訪問を参照画面に表示する方法を構成する

- アプリにいくつかの基本的な変更を加える

- アプリの機能をテストする

## <a name="prerequisites"></a>前提条件

- **モジュール 0 ラボ 0 - ラボ環境の検証** の完了
- **モジュール 2 ラボ 1 - データ モデリング** の完了

## <a name="exercise-1-create-visits-canvas-app"></a>演習 1:訪問キャンバス アプリを作成する

**目的:** この演習では、以前に作成した訪問テーブルを接続して、キャンバス アプリを作成します。

### <a name="task-1-create-the-visits-app"></a>タスク \#1:訪問アプリを作成する

1.  <https://make.powerapps.com> に移動します。 再認証が必要な場合は、**[サインイン]** をクリックし、必要に応じて指示に従ってください。

2.  **[[自分のイニシャル] 練習]** 環境がまだ選択されていない場合は、右上で選択します。

3.  画面の左側にある **[ホーム]** アイコンをクリックし、**[Dataverse]** アイコンを選択します。

4.  Dataverse 接続を選択します。

    > **注:** *"Dataverse 接続が存在しない場合:"*
    > - **[新しい接続]** を選択します
    > - **[Microsoft Dataverse]** を見つけます
    > - **[作成]**

5.  前のラボで作成した **[訪問]** テーブルを見つけて選択します。

6.  右下隅にある **[接続]** ボタンをクリックします。

7.  アプリが作成されたら、[Power Apps Studio へようこそ] 画面で、 **[今後は表示しない]** ボックスをオンにし、 **[スキップ]** を選択します。

8.  作成が完了したら、次の図のような画面が表示されます。

![訪問データから作成されたキャンバス アプリ。](media/2-canvas-app-from-data.png)

9. アプリデザイナーのコマンドバーで、 **[アプリのプレビュー]** ボタン (右上の再生アイコン) を選択します。 *(キーボードの F5 キーを押してアプリをプレビューすることもできます)。* アプリがすぐに使用できる状態であることを確認します。

10. 画面の右上にある **×** を選択して、アプリのプレビューを閉じます。

これで、Dataverse テーブルから Power App が正常に作成されました。 プロセスの次のステップとして、カレッジのブランド化に合わせてアプリを調整します。 次の一連の手順では、いくつかの点でアプリをさらにカスタマイズする手順について説明します。

### <a name="task-2-modify-and-theme-the-newly-created-app"></a>タスク \#2:新しく作成したアプリのテーマを変更する

このタスクでは、アプリの 3 つの各画面 ([参照]、[詳細]、[編集]) のヘッダー テキストをカスタマイズし、アプリ テーマを変更します。

1.  画面上の **[訪問]** ラベルを選びます。

1.  画面の右側にある [プロパティ] タブで、**[テキスト]** プロパティを "**ベローズカレッジの訪問**" に更新します。

1. [プロパティ] タブの、 **[フォント サイズ]** を **[24]** に変更します。

1.  画面の空白の背景をクリックすると、参照画面に更新されたテキストが表示されます。

1.  左側のナビゲーションのツリービューから、 **[DetailScreen1]** を選択します。

1.  画面上の **[訪問]** ラベルを選びます。

1.  画面の右側にある [プロパティ] タブで、**[テキスト]** プロパティを **"訪問の詳細"** に更新します。

1.  画面の空白の背景をクリックすると、詳細画面に更新されたテキストが表示されます。

1.  左側のナビゲーションにあるツリービューから、 **[EditScreen1]** を選びます (ツリービューでこれを表示するには、必要に応じて下にスクロールする必要がある場合があります)。

1.  画面上の **[訪問]** ラベルを選びます。

1.  画面の右側にある [プロパティ] タブで、**[テキスト]** プロパティを **"詳細の編集"** に更新します。

1.  画面の空白の背景をクリックすると、編集画面に更新されたテキストが表示されます。

1. 左側のナビゲーションにあるツリー ビューを使用して、 **[BrowseScreen1]** を選択します。

1. コマンドツールバーで、 **[テーマ]** ボタンを選択し、表示された一覧から、テーマの色として **[赤]** を選択します。

### <a name="task-3-test-your-visits-app"></a>タスク \#3:訪問アプリをテストする

このタスクでは、新しいアプリをテストします。

1.  アプリ デザイナーでアプリケーションを開いた状態で、**[設定]** を選択し、アプリの名前を **[訪問アプリ]** に更新して、**×** を選択します。**[Ctrl + S]** を押すと[名前を付けて保存]の画面が表示されるので **[保存]** を選択します。

3.  左側のナビゲーションから、 **[BrowseScreen1]** を選択します。

4.  アプリ デザイナーのコマンド バーで、 **[アプリのプレビュー]** ボタン (再生アイコン) を選択します。 *(キーボードの F5 キーを押してアプリをプレビューすることもできます)。*

4.  アプリが開いたら、**[検索アイテム]** フィールドに、テキスト「 **Maria** 」を入力します。 (検索フィールドに入力された内容に基づいて、ギャラリー内の項目がどのようにフィルター処理されるかに注目してください)

5.  **Maria Campbell** の **Contoso Suites** レコードなどが表示され、行をクリックすると、その詳細が表示されます。 (**注**: *Maria Campbell の Contoso Suites レコードが複数表示される場合、いずれかを選択します)*

6.  レコードを編集するには、アプリの右上隅にある **鉛筆アイコン** を選択します。

7.  ここで [Visit Name(訪問名)] を編集することができます。右上隅のチェックマークアイコンをクリックすると、変更を保存することができます。

8.  画面の右上隅にある **×** アイコンをクリックすると、キャンバスアプリエディターに戻ります。

お疲れさまでした。 最初のキャンバス アプリの作成と構成が完了しました。

## <a name="challenges"></a>課題

- [DetailScreen1] と [EditScreen1] のフォームに列 [実際の開始]、[実際の終了]、[コード]、[開始予定]、[終了予定] を追加してみましょう

[次の章へ(ラボ3)](https://github.com/hamabe-12/PL-900/blob/main/Instructions/Labs/LAB%5BPL-900%5D_M03Lab03_Model_App.md)