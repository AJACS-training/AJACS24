#  はじめに [#dd357d3d]

- マイクロアレイデータの解釈
    - IPA(Ingenuity Pathways Analysis)やMetaCoreといったパスウェイ解析ソフトウェア（多くは有償）
    - Reactome http://www.reactome.org/ がだんだんよくなってきている
- ゲノム配列データの解釈
    - 複数のゲノムアノテーション情報を組み合わせて活用→候補遺伝子・領域の抽出（今日は主にこれ）
    - ChIP-seqデータの解析 → 次世代GeneSpringのAvadisNGSなどのソフトウェアで

#  Biomart [#fcada5ef]

##  【実習1】Biomartを使い倒す～遺伝子の上流配列を取得する [#r3aeb7ed]
- [[【使い方参考動画】>http://togotv.dbcls.jp/20090327.html#p01]]http://lifesciencedb.jp/image/small_video_icon.png


- 1. [[http://www.biomart.org/>http://www.biomart.org/]]を開きます。
- 2.リスト中の[[Ensembl>http://www.ensembl.org/biomart/martview]]をクリックします。
- 3. 「-CHOOSE DATABASE-」のプルダウンメニューを「Ensembl Genes 61」に設定します。
- 4. 「-CHOOSE DATASET-」のプルダウンメニューを「Homo sapiens genes (GRCh37.p2)」に設定します。
- 5. 左端の「Filters」をクリックし、出現する「GENE」の＋ボタンをクリックして展開します。
- 6. 「ID list limit」にチェックを入れ、「Affy hg u133a ID(s)」を選択し、「参照」ボタンを押して[[このファイル>http://motdb.dbcls.jp/?plugin=attach&refer=AJACS12%2Fhono3&openfile=090907_sample_U133A_adipo.txt]]を選択します。
- 7. 「Attributes」をクリックして、「Sequences」にチェックを入れます。
- 8. 「SEQUENCES」の＋ボタンをクリックし、「Flank (Gene)」をチェックし、「Upstream flank」にチェックを入れ、その右に「1000」と入力します。
- 9. 左端上部の「Count」をクリックすると、これまで設定した条件に該当する数がわかります。（今回の設定では405 / 53630 Genes）
- 10. 「Results」をクリックし、「Export all results to」を「Files」（ファイル容量が大きい場合は「Compressed file(.gz)」を選択するとよい）を選択し、「Go」をクリックします。


## 【応用1】Biomartを使って、マイクロアレイデータのIDに対応したGO termのリストを取得する [#a83d5bfe]
- [[【使い方参考動画】>http://togotv.dbcls.jp/20090225.html#p01]]http://lifesciencedb.jp/image/small_video_icon.png

- 1. [[http://www.biomart.org/>http://www.biomart.org/]]を開きます。
- 2.リスト中の[[Ensembl>http://www.ensembl.org/biomart/martview]]をクリックします。
- 3. 「-CHOOSE DATABASE-」のプルダウンメニューを「Ensembl Genes 61」に設定します。
- 4. 「-CHOOSE DATASET-」のプルダウンメニューを「Homo sapiens genes (GRCh37.p2)」に設定します。
- 5. 左端の「Filters」をクリックし、出現する「GENE」の＋ボタンをクリックして展開します。
- 6. 「ID list limit」にチェックを入れ、「Affy hg u133a ID(s)」を選択し、「参照」ボタンを押して先ほど保存した「090907_sample_U133A_adipo.txt」を選択します。
- 7. 「Attributes」をクリックして、「GENE」のなかの「Ensembl Gene ID」、「Ensembl Transcript ID」のチェックをはずします。
- 8. 続いて、「EXTERNAL」の＋ボタンをクリックし、「 go biological process」中の「Gene Ontology Accession」にチェックを入れます。
- 9. 左端上部の「Count」をクリックすると、これまで設定した条件に該当する数がわかります。（今回の設定では408 / 44285 Genes）
- 10. 「Results」をクリックし、「Export  all results to」を「Files」（ファイル容量が大きい場合は「Compressed file(.gz)」を選択するとよい）と「TSV」（タブ区切りテキスト）を選択し、「Go」をクリックします。
- 11. 「mart_export.txt」というファイルがダウンロードされるので、デスクトップに保存し、「090907_U133A_adipo_GO.txt」とファイル名を変更します。

うまくダウンロードできない場合は下記のファイルを使用してください。
#ref(AJACS12/hono3/090907_U133A_adipo_GO.txt,left)
（右クリックして「名前を付けてリンク先を保存」してください。）


#  Galaxy [#pceafd95]

##  【実習2】Galaxyを使って、特定の転写因子予測結合領域と遺伝子上流領域の「交差点」をリストアップする [#bc92a728]
- [[【使い方参考動画】>http://togotv.dbcls.jp/20090310.html#p01]]http://lifesciencedb.jp/image/small_video_icon.png

- 1. [[http://galaxy.dbcls.jp/>http://galaxy.dbcls.jp/]]を開きます。
- 2. 画面左にあるToolsカラムの「Get Data」をクリック
- 3. 画面左にあるToolsカラムの「UCSC Main」をクリックすると、真ん中にUCSC Genome Browserの画面が表示されます。
- 4. 以下のパラメータを設定してから、'get output'をクリック
    - clade: Mammal
    - genome: Human
    - assembly: Mar. 2006
    - group: Genes and Gene Prediction Tracks
    - track: UCSC Genes
    - table: knownGene
    - region: genome
    - output format: BED
    - Send output to 'Galaxy'にチェック
- 5. Create one BED record per: で 'Upstream by'にチェック。今回はデフォルトのまま、'200'basesを指定します
- 6. 'Send query to Galaxy'をクリック
- 7. 画面右にあるHistoryカラムに注目し、緑色に変化するまで待ちます
- 8. タイトルをクリックすると、詳細が表示されます
- 9. 画面左にあるToolsカラムの'UCSC Main'を再度クリック
- 10. 以下のパラメータに変更
    - group: Regulation
    - track: TFBS conserved
    - table: tfbsConsFactors
- 11. tableの説明を見るには、すぐ右にある'describe table schema'ボタンをクリック。その画面から戻るには、ブラウザの戻るボタンを使用します。
- 12. filter:の右の'create'ボタンを押して、出てきた画面のspecies に'human'と入力して'submit'ボタンをクリック。ヒトのデータだけにフィルタリングを行います
- 13. Send output to 'Galaxy'のチェックを外して'get output'をクリックすると、ヒトのデータだけにフィルタされたtfbsConsFactorsに登録されているヒトの転写因子がリストされます
- 14. ブラウザの検索機能を利用して'p53'で検索して、p53関連のエントリ名を調べます。それのうち'V$P53_'をコピーして、前の画面に戻ります。
- 15. table: tfbsConsSites に設定を変更し、filterで'create'をクリック
- 16. nameフィールドに先ほどコピーした'V$P53_'を貼り付けます。その際、最初から入力されている'*'を上書きせず残して、その文字の前に貼り付けて、submitします
- 17. output format: BED に変更して、Send output to Galaxyにチェックを入れて'get output'をクリック
- 18. そのまま'Send query to Galaxy'をクリック
- 19. 画面右のHistoryカラムに注目し、緑色に変化するまで待ちます
- 20. タイトルをクリックすると、詳細が表示されます。例えば、24,601箇所p53結合サイトと予測された領域があることが分かります
- 21. このデータセット（p53予測結合領域）と先ほど用意したデータセット（ヒト遺伝子すべての上流200bpの領域）の重なりを画面左のToolsカラムにある'Operate on Genomic Intervals'メニューから調べてみましょう
- 22. 'Operate on Genomic Intervals'をクリックして出てくる'Intersect..'をクリック
- 23. second queryに'1. UCSC Main...'をセットし、'Execute'をクリック
- 24. 画面右のHistoryカラムに注目し、緑色に変化するまで待ちます
- 25. タイトルをクリックすると、詳細が表示され、535箇所オーバーラップがあったことが分かります
- 26. 目のマークをクリックすると計算結果が表示されます
- 27. 計算結果の中の'display at UCSC main'の'main'をクリックすると得られた領域がUCSC Genome Browser上で見ることができます

##  【応用2】Galaxyを使って、あるIDに対応する別のIDをデータに付加する＆解析結果・方法を共有する [#rcfffb68]
- [[【使い方参考動画】>http://togotv.dbcls.jp/20101116.html#p01]]http://lifesciencedb.jp/image/small_video_icon.png
