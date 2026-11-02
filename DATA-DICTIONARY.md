# 資料字典

book.json為固定主本，pages[]的fXX是19個官方影像幀；unit ID的pXX是31個目標物理面，不等於原刻頁碼。p02為明確排除的鏡像透印，非漏頁。unit.layer均original-print，role保存原正文、細註、圖字及附文角色，bbox=null，沒有逐字座標。

running_title、printed_page_number及other_paratext各投影一次；附文資料序不是物理座標。methods.physical_faces保存原版面metadata，不再拼成第二份正文。原units.order由陣列序保存。

methods.initial_metadata與notes保留已核公開原稿欄位；source_reading_records整欄含私路徑而排除。公開projection與完整私檔不是同bytes。7筆uncertainty_id_aliases僅將舊ID映到現有margin/folio unit，原字串／target／candidates／reason不變。

uncertainties以unit_id及Unicode碼點0起半開區間[start,end)定位，surface=text[start:end]，extent=known只表位置，不表定讀。candidates不替換正文。

source-regions.json與methods.unresolved_source_regions保存1個非文字區域、原圖bbox、官方定位、unknown extent及text=null／missing_character_count=null；reason／state是已看但未解，不是未處理。TEI透過declared-methods快照承載，不在body虛造字串或gap字數。

341主單位與58附文metadata投影單位，合計399原印文字單位、6538Unicode碼點、32筆文字疑讀；另有1個已查看但來源／範圍未定的p12狹窄頁邊片段。未解區沒有猜補字串或缺字數，不是未處理頁。碼點數不是漢字數，疑讀數不是錯誤率。
