# データベースとは
データベースとは、文字や数値などのデータを管理する仕組みのことをいいます。データベースを使うと欲しい検索条件でデータを見つけることができます。

## データベースはどうやって動いている？
データベースは専用のデータベースソフトウェアで動いています。Microsoft OfficeについているAccessや、Filemakerなどがデータベースソフトウェアです。
それ以外に、サーバー上で動作させて使う、MySQLやPostgres SQL、Orcaleデータベースなどがあります。

### データベースの中身
データベースの中身は、複数の「テーブル」というExcelのシートのようなものでできています。例えば、果物の商品名、商品価格を管理する商品管理テーブルと販売数量を管理するテーブルは以下のようになります。

商品管理テーブル

|商品番号|名前|価格|
|:--:|:--:|:--:|
|1|りんご|150|
|2|みかん|100|
|3|ばなな|200|

販売数量管理テーブル

|商品番号|販売数量|
|:--:|:--:|
|1|30|
|2|25|
|3|20|

販売数量管理テーブルの方には商品名がありませんが、両方に同じ商品番号があるので、それらで関連づけることで、商品番号1番のりんごの販売数量が30であることがわかります。

これは単純な例なので、販売数量の列を商品管理の右端に追加するだけの方がいいと思われるかもしれませんが、実際には販売数量は月ごととか年ごとのように増えることがあったり、ひとつのテーブルにすると販売が終了している商品の販売数量まで記録するための領域が必要になりデータサイズ（0でもデータはデータなので）が大きくなるため複数に分ける方がメリットがある場合ああります。
テーブルをどのように分けるか？ということに決まりはなく、管理したいデータをどのように使いたいかでその都度決めます。

## データベースを使うメリット
データベースは、データを管理することに特化したシステムなので大量のデータを管理していても表示や検索が速いというメリットがあります。
Excelでも同じようにデータを管理することはできますが、データ量が大きくなると重くなり使えなくなります。

## どんなところでデータベースは使われている？
身近なところでは、会員情報の管理やECサイトの商品管理などに使われています。
Google検索でもデータベースは使われています。
ただし、Google検索の場合は大量のwebサイトの情報を管理していて、これを速く、そして利用者が入力した複数のキーワードで検索できるように複雑なテーブルの分け方や設計になっていると思います。

