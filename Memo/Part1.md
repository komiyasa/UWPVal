https://docs.microsoft.com/ja-jp/windows/apps/desktop/modernize/modernize-wpf-tutorial-1

Contoso の経費のサンプルアプリを入手する
4. [スタート] ボタンまたは CTRL キーを押しながら F5 キーを押して、Contoso の経費の WPF プロジェクトをビルド、実行、およびデバッグできることを確認します。
<コメント>
->クラスライブラリの出力タイプを持つプロジェクトを直接起動することはできませんエラーが発生するかも？
その場合は、実行可能なプロジェクト名（それまでビルドできていたプロジェクトがあればそのプロジェクト名）を右クリックして、「スタートアッププロジェクトに設定」をクリック


作業 1:Contoso Expenses　アプリの .NET Core 3 への移行
ContosoExpenses プロジェクトを .NET Core 3 に移行する
2.Windows エクスプローラーで、 C:\WinAppsModernizationWorkshop\Lab\Exercise1\01-Start\ContosoExpensesフォルダーに移動し、 ContosoExpensesという名前の新しいテキストファイルを作成します。
<コメント>
-> 日本語が分かりにくい。正しくは、「ContosoExpenses.Core.csproj」というファイルを作成する。
In Windows Explorer, navigate to the C:\WinAppsModernizationWorkshop\Lab\Exercise1\01-Start\ContosoExpenses folder and create a new text file named ContosoExpenses.Core.csproj.


ContosoExpenses プロジェクトを .NET Standard に移行します。
<コメント>
->正しくは ContosoExpense.Data プロジェクト
下記日本語訳にも間違いがあります。
1. Visual Studio で、 ContosoExpensesプロジェクトを右クリックし、[プロジェクトのアンロード] を選択します。 プロジェクトをもう一度右クリックし、 [ContosoExpenses の編集] を選択します。
->（下記英語が正しい）
1. In Visual Studio, right-click the ContosoExpenses.Data project and choose Unload Project. Right-click the project again and then choose Edit ContosoExpenses.Data.csproj.
4. ContosoExpensesプロジェクトを右クリックし、[プロジェクトの再読み込み] をクリックします。
->(下記英語が正しい)
4. Right-click the ContosoExpenses.Data project and choose Reload Project.
※これ以下のドキュメントでも「ContosoExpense」と「ContosoExpense.Data」の記載違いがあります。基本的には英語ドキュメントに従った方が良いかもしれません。

NuGet パッケージと依存関係の構成
<コメント>
検証した際の Nuget パッケージの Latest Version を以下に纏めます。
Bogus 28.4.1
LiteDB 4.1.4
Unity Latest Version 5.11.1
MvvmLightLibsStd10 5.4.1.1
Microsoft.Windows.Compatibility 3.0.1


1. ContosoExpensesプロジェクトで、 app.configファイルを開きます。 現在、.NET Framework 4.7.2 を対象とする次の参照が含まれていることに注意してください。
<コメント>
->(下記英語が正しい)
In the ContosoExpenses.Core project, open the packages.config file. Notice that it currently contains the following references that target the .NET Framework 4.7.2.
※日本語では「ContosoExpense」となっていますが、ただしくは「ContosoExpense.Core」です。


