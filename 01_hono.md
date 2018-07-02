遺伝子発現データベースの活用法
担当：小野浩雅

~目次
#contents

# 遺伝子発現データベースに関する統合TV
- [統合TVの「発現情報」タグをクリック！](http://togotv.dbcls.jp/?category=%C8%AF%B8%BD%BE%F0%CA%F3)
- [統合TV Curatedの発現制御解析から探す](http://togotv-curated.dbcls.jp/contents/category/expression#%E9%81%BA%E4%BC%9D%E5%AD%90%E3%83%BB%E3%82%BF%E3%83%B3%E3%83%91%E3%82%AF%E8%B3%AA%E7%99%BA%E7%8F%BE%E3%82%92%E7%B6%B2%E7%BE%85%E7%9A%84%E3%81%AB%E8%AA%BF%E3%81%B9%E3%81%9F%E3%81%84)

# [BioGPS](https://biogps.gnf.org/)
ヒト、マウス、ラットのさまざまな組織や細胞(株)における遺伝子発現プロファイルのデータベース

- [[BioGPS>https://biogps.gnf.org/]]はAffymetrix社製のマイクロアレイであるGeneChipを用いた遺伝子発現プロファイルのデータベース。
- [[GNF SymAtlas>http://symatlas.gnf.org/]][[【参考動画】>http://togotv.dbcls.jp/20070816.html]]のメジャーアップデート版。
- マウスのエキソンアレイのデータが追加されたので、遺伝子のスプライシングバリアント(Splicing variant)の発現状況も調べることが可能。
- 検索した遺伝子に対して、種々の外部データベースに横断検索することができる。
## 【実習1】BioGPSを使ってある遺伝子の発現プロファイルを調べる [#k6b911bc]
- [[【使い方参考動画】>http://togotv.dbcls.jp/20110120.html#p01]]、[[【講習会動画】>http://togotv.dbcls.jp/20100829.html#p01]]http://lifesciencedb.jp/image/small_video_icon.png
- 1. [[https://biogps.gnf.org/>https://biogps.gnf.org/]]を開きます。
- 2.骨格筋の分化決定遺伝子であるMyogenic differentiation 1(MyoD)の発現プロファイルを調べてみましょう。中央の検索窓に「myod」と入力し、「search」を押します。
- 3. 表示された検索結果の中から「ID 4654」をクリックします。
- 4. 最初はヒトのマイクロアレイデータが表示されます。
- 5. 画面左側の三角形をクリックすることでサイドバーを非表示にできます。非表示にすることで画面を広く使うことができます。
- 6. ページ内のウインドウは通常のウインドウと同じようにドラッグによる移動やサイズの変更などを行うことができます。 歯車マークのメニューから"Open in Browser" を選択すると、新しいタブで表示できます。
- 7. "Search" と書かれた窓に単語(組織名など)を入力すると、その単語の含まれた部分が赤くハイライト表示されます。今回は "Muscle" と入力してみます。
- 8. "Zoom" のバーを用いることで、グラフの表示範囲を調整することが出来ます。
- 9. 発現量を示すバーをクリックすると発現強度の値が表示されます。
- 10. マイクロアレイデータ右上の「Species: Hs」をクリックするとマウスやラットを選択できるので、「M. musculus (Mouse)」をクリックしてマウスのデータを表示できます。
- 11. MyoDはどの組織、細胞で強く発現しているでしょうか？
- 12. "Static Image" をクリックすると、ズームや検索機能などのついていない、画像だけのグラフで表示されます。低スペックなマシンでは、こちらの方が軽快に動作するでしょう。
- 13. 場合によっては右端のプルダウンメニューから複数の項目を選択できる場合があります。これはどのようなケースが考えられるでしょうか。
- 14. 「Correlation」タブをクリックして検索すると、発現パターンが似ている他の遺伝子を検索できますが、どのような遺伝子が出てくるでしょうか？
- 15. "Downloads" をクリックすると現在表示しているデータを CSV 形式でダウンロードできます。


- 16. 右上の「default rayout」をクリックすると、検索した遺伝子に関するマイクロアレイデータ以外のデータが閲覧できますが、どのようなデータが閲覧できるのか調べてみましょう。
- 17. 左上の「Search」タグをクリックして検索画面にもどり、自分の興味ある遺伝子について同様に検索してみましょう。
すぐに自分の興味ある遺伝子が浮かばない場合は、話題の[[iPS細胞>http://ja.wikipedia.org/wiki/%E4%BA%BA%E5%B7%A5%E5%A4%9A%E8%83%BD%E6%80%A7%E5%B9%B9%E7%B4%B0%E8%83%9E]]を作るために必要な4因子（Oct3/4・Sox2・Klf4・c-Myc）がどの組織で発現しているかを検索してみましょう。

- 【余談】
BioGPSのiPhoneアプリが無料で公開されていますので、「あの遺伝子はどの組織で発現してるのかな？」とふと思いついたときにお手持ちのiPhoneで遺伝子発現を調べられます。


# [[&size(20){DAVID: The Database for Annotation, Visualization and Integrated Discovery};>http://david.abcc.ncifcrf.gov/]] [#zef09660]
&color(green){マイクロアレイデータの生物学的な解釈};

http://david.abcc.ncifcrf.gov/

- マイクロアレイ実験の一般的な目的は、実験条件によって得られたある遺伝子群の発現が生物学的にどういう意味を持つかを考えることです。
#ref(AJACS14/thecla/microarray.analysis.005.png)
- 今回は、その方法の一つとして、マイクロアレイの結果に[[Gene Ontology>http://www.google.co.jp/url?sa=t&source=web&cd=4&ved=0CEEQFjAD&url=http%3A%2F%2Fja.wikipedia.org%2Fwiki%2F%25E9%2581%25BA%25E4%25BC%259D%25E5%25AD%2590%25E3%2582%25AA%25E3%2583%25B3%25E3%2583%2588%25E3%2583%25AD%25E3%2582%25B8%25E3%2583%25BC&ei=ve9QTd6XMtG6cbeW1KUH&usg=AFQjCNF8U-O4ktlMGoR9DNC0wKltmbjtmw]]の用語を付与することで、生物学的な解釈を行います。
- 【参考動画】[[DAVIDを使ってマイクロアレイデータを解析する>http://togotv.dbcls.jp/20090925.html#p01]]http://lifesciencedb.jp/image/small_video_icon.png

## マイクロアレイデータの準備 [#z6529d62]
サンプルデータとして、[[NCBI GEO>http://www.ncbi.nlm.nih.gov/geo/]]より取得した公共の遺伝子発現データを用います。このデータは、ある実験の前後の2群間で有意に発現減少した遺伝子群のリストです。
#ref(AJACS24/hono/110208_IDlist.txt,left)
（右クリックして「名前を付けてリンク先を保存」してください。）
<br>
このデータは、どのような実験から得られたデータなのか、どのように解釈できるのかをDAVIDを使って考察してみましょう！

## 【実習2】DAVIDを用いて、発現データの結果を生物学的に解釈する [#y04a402a]
- 1. 上部メニューの「Start Analysis」をクリックします。
- 2. 画面左側バーで、probe IDリストをコピペ or ファイルを指定します。
- 3. リストのIDの種類タイプを選択します。 … 今回は、「AFFY_ID」と「Gene List」
- 4. Submit List をクリックするとリストが読み込まれます。
- 5. アップロードしたリストは、左側バーの「List Manager」で「Uploaded List_1」として保存されています。削除やrenameもできます。
- 6. 解析を続けます。真ん中の「Functional Annotation Tool」をクリックします。
- 7. 「Gene Ontology」をクリックすると、Gene Ontologyを用いた解析の細かいメニューが表示されます。
- 8. 今回は、GOTERM_BP_FAT (BP=Biological Process)に注目します。その右の「Chart」をクリックすると結果がポップアップされます。
- 9. P-value を2回クリックしてp-valueが小さい（統計的に有意である）順にしてみましょう … p-value小さい順は、一度やればしばらく覚えているので、次からはしばらくは必要ないです
#fold(結果,#ref(AJACS24/hono/david_go_bp.png));
- [応用編] Pathways > KEGG_PATHWAY や Tissue Expression > UP_TISSUE なども見てみましょう。生物学的にどういうことが言えるでしょうか。


        --


# [[&size(20){NCBI Gene Expression Omnibus (GEO)};>http://www.ncbi.nlm.nih.gov/geo/]] [#r6287e42]
&color(green){世界最大の遺伝子発現（[[マイクロアレイ>http://ja.wikipedia.org/wiki/DNA%E3%83%9E%E3%82%A4%E3%82%AF%E3%83%AD%E3%82%A2%E3%83%AC%E3%82%A4]]）データベース（レポジトリ）};


## 【発展編・実習3】GEOを使って、自分の興味のある遺伝子の（ある実験条件下における）発現状況を調べる [#a83d5bfe]
- [[【使い方参考動画】>http://togotv.dbcls.jp/20090213.html#p01]]http://lifesciencedb.jp/image/small_video_icon.png
- 1. [[http://www.ncbi.nlm.nih.gov/geo/>http://www.ncbi.nlm.nih.gov/geo/]]を開きます。
- 2.「Gene profiles」に自分の検索したい遺伝子名を入力します。
- 3. 今回は例として「[[nanog>http://www.google.co.jp/search?hl=ja&q=Nanog%E9%81%BA%E4%BC%9D%E5%AD%90]]」という遺伝子を検索してみましょう。入力終了後、「GO」をクリックします。
- 4. GEOに登録されている様々な実験条件で行なわれたマイクロアレイ実験における「nanog」遺伝子の発現データが表示されます。
- 5. 検索結果の右端にある画像をクリックすると、[[発現データの詳細をみる>http://www.ncbi.nlm.nih.gov/geo/gds/profileGraph.cgi?&dataset=DEAryz&dataset=yyyzzz$&gmin=5173.000000&gmax=11680.000000&absc=&gds=2294&idref=161072_at&annot=Nanog]]ことができます。
- 6. 「Display values」をクリックすると、発現値を一覧できます。
- 7. [[このサンプル>http://www.ncbi.nlm.nih.gov/sites/GDSbrowser?acc=GDS2294]]では、nanogはどういう細胞のどういう実験条件で発現が増減しているか調べてみましょう。
- 8. ページ下部の「samples」に列挙された[[リンク>http://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSM130365]]をクリックすると、そのサンプル（一枚のマイクロアレイ）の詳細を閲覧できます。
- 9. [[リンク先のページ>http://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSM130365]]の中ほどにある[[「series」のリンク>http://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE5583]]をクリックすると、この実験全体の詳細情報が見られます。
- 10. [[この実験全体の詳細情報ページ>http://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE5583]]の下部にある[[「Series Matrix File(s)」>ftp://ftp.ncbi.nih.gov/pub/geo/DATA/SeriesMatrix/GSE5583/]]をクリックすると、この実験の正規化補正済みのマイクロアレイデータをダウンロードすることができます。
## 【発展編・実習4】データセットブラウザ(Dataset browser)を利用して、GEOに登録されているマイクロアレイデータを解析する [#mcb0ec77]
- [[【使い方参考動画1】>http://togotv.dbcls.jp/20090221.html#p01]]http://lifesciencedb.jp/image/small_video_icon.png 、[[【使い方参考動画2】>http://togotv.dbcls.jp/20090307.html#p01]]http://lifesciencedb.jp/image/small_video_icon.png
- 1. [[http://www.ncbi.nlm.nih.gov/geo/>http://www.ncbi.nlm.nih.gov/geo/]]を開きます。
- 2.「Gene profiles」に自分の検索したい遺伝子名を入力します。
- 3. 今回は例として「[[nanog>http://www.google.co.jp/search?hl=ja&q=Nanog%E9%81%BA%E4%BC%9D%E5%AD%90]]」という遺伝子を検索してみましょう。入力終了後、「GO」をクリックします。
- 4. GEOに登録されている様々な実験条件で行なわれたマイクロアレイ実験における「nanog」遺伝子の発現データが表示されます。
- 5. 検索結果の[[アクセッション番号（今回は GDS2294）>http://www.ncbi.nlm.nih.gov/sites/GDSbrowser?acc=GDS2294]]をクリックすると、解析用の「データセットブラウザ」が開きます。
- 6. 「Expression profiles」をクリックすると、[[この実験データセットにおける個々の遺伝子発現状況を検索できるページ>http://www.ncbi.nlm.nih.gov/sites/entrez?db=geo&cmd=search&term=GDS2294[ACCN]]に飛びます。
- 7. 検索窓に表示されているアクセッション番号の後に続けて遺伝子名を追加（今回は例として [[Oct4>http://www.google.co.jp/search?q=Oct4]] ）すると、この実験データセット内におけるその遺伝子の発現データが検索できます。
- 8. 「データセットブラウザ」の「Data Analysis Tools」では詳細なデータ解析が可能です。
- 9. 「Find gene name or symbol:」のところに自分の興味ある遺伝子名を入れてみましょう。
- 10. 「Find genes that are up/down for this condition(s):」の「GO」をクリックするとどのような遺伝子がヒットするでしょうか。
- 11. 「Compare 2 sets of samples」では2群間で発現に差のある遺伝子を（統計学的に）検索できます。step1で発現量の違いを検出する方法を設定します。step.2で比較する2群の設定をします。step.3の「Query Group A vs. B」をクリックすると、検索が始まります。
- 12. 「Cluster heatmaps」では、マイクロアレイデータ解析でよく用いられる[[ヒートマップ>http://images.google.co.jp/images?q=ヒートマップ]]でのデータ表示が行なえます。分類方法としてHierarchical、Partitional (K-means/K-medians)、By location on chromosomeの3種類が選べますが、それぞれどのようにデータが分類されるか試してみましょう。
- 13.  「Experiment design and value distribution」では実験データにおける発現の分布を参照できます。これにより、各サンプルのデータが互いに比較可能か（実験上のミスがないか）チェックすることができます。




## 【発展編・実習5】GEOを使って、自分の興味のあるマイクロアレイ実験データセットを検索&生データをダウンロードする [#ze44dc22]
- [[【使い方参考動画】>http://togotv.dbcls.jp/20081218.html#p01]]http://lifesciencedb.jp/image/small_video_icon.png
- 1. [[http://www.ncbi.nlm.nih.gov/geo/>http://www.ncbi.nlm.nih.gov/geo/]]を開きます。
- 2. 画面中央の「Platforms」をクリックします。
- 3. [[Platform(マイクロアレイの種類)の一覧画面が現れる>http://www.informatics.jax.org/javawi2/servlet/WIFetch?page=imageSummaryByMrk&key=25000&imageType=8]]ので、上部の「FIND PLATFORM」をクリックします。
- 4. [[platformの検索画面>http://www.ncbi.nlm.nih.gov/geo/query/browse.cgi?mode=findplatform]]が現れるので、「Company name」に「Affymetrix」、「organism」に「Homo sapiens」を選択し、「FIND PLATFORM」をクリックします。
- 5. [[Affymetrixのヒトのマイクロアレイの検索結果>http://www.ncbi.nlm.nih.gov/geo/query/browse.cgi?mode=foundplatform]]が表示されるので、中程にある「Affymetrix GeneChip Human Genome U133 Plus 2.0 Array」の左端にある[[「GPL570」というID>http://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GPL570]]をクリックします。
- 6. [[表示された画面>http://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GPL570]]の真ん中あたりにある「series」下の「More...」をクリックすると、登録されているデータセットを閲覧できます。
- 7. ブラウザの検索ボタンなどを使って「reprogramming」という単語を検索するとどういうデータがヒットするでしょうか？
- 8. ヒットしたデータの左端にあるIDをクリックすると、[[そのデータセットの詳細情報>http://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE9832]]が閲覧できます
- 9. ページ下部の「Download family」の中にある「Series Matrix File(s)」をクリックすると正規化済みのデータのダウンロードリンクが表示されます。
- 10. ページ最下部の「Supplementary file」にあるリンクから生データをダウンロードすることができます。
- 11. 自分の研究テーマに近い、また興味のあるマイクロアレイデータが利用可能か検索してみましょう。

# 【参考1】[[遺伝子発現バンク(GEO)目次、通称「GEO目次」>http://lifesciencedb.jp/geo/]] [#rdfd50d4]
- [[使い方参考動画>http://togotv.dbcls.jp/20080623.html#p01]] http://lifesciencedb.jp/image/small_video_icon.png
- NCBI GEO を日本語のインターフェイスで快適に使い、データの全容を俯瞰するための仕組み
- 検索が便利！

# 【参考2】[[RefEX>http://togoexp.dbcls.jp/RefEx/human/]] [#e22736da]
- [[使い方参考動画>http://togotv.dbcls.jp/20100618.html#p01]]http://lifesciencedb.jp/image/small_video_icon.png
- RefEx （Reference Expression dataset）は、ライフサイエンス統合データベースセンター（DBCLS）が提供する4種類の異なる手法 （EST, GeneChip, iAFLP, CAGE）によるヒトおよびマウスの遺伝子発現データのリファレンスデータセットです。複数の手法による客観的な遺伝子発現データの比較が可能となるウェブインターフェースが用意されていることに加えて、個々の遺伝子については染色体領域や遺伝子ファミリー（InterPro）、Gene Ontology に基づく生物学的機能別に検索ができる他、発現パターンから探すことが可能になっています。
- 現在もさらに使いやすくなるようアップデート作業中です。
