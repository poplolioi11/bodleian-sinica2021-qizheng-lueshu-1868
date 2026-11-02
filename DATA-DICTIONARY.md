# 資料字典

pages[]為19個fXX官方影像幀；pXX為物理面，非原刻頁碼。每單位layer=original-print，role區分正文／細註／圖字／版心／頁碼／附文；bbox=null，無逐字座標。

19幅固定官方3000×2627影像、31目標物理面（p01及p03–p32）；p02鏡像透印只描述不反轉重錄，p30無正文的原印版心層仍收，具體字串依本版採文；p11、p12、p25、p26圖面文字納入但不重建圖形幾何。

398原印文字單位／6536Unicode碼點，35文字疑讀與35個已看但來源／範圍未解區分列；pending=0。相對初錄47既有單位字串變動、1新增、2刪除，新增中1筆具split_from關係。這些不是錯字數或準確率，初錄快照不計入本版文字數量。

本版單位與次序以凍結canonical為準，增刪及split_from由精確ledger核對，不硬套399舊ID。methods.physical_faces是metadata，不重複拼成正文。

methods.initial_version_snapshot.public_book是已發布v1完整JSON值；published_book_sha256描述原檔bytes，與嵌入JSON值相等分開。快照不含私有source_reading_records；初錄7 aliases保留歷史意義，不算訂正。

疑讀[start,end)以Unicode碼點0起定位，surface=text[start:end]，候選不替換正文。source-regions.json與methods.unresolved_source_regions值相同，extent=unknown、text=null、missing_character_count=null；bbox為原圖區域，不是逐字框。

TEI declared-methods保留同一metadata快照，body不虛造未知文字／gap字數；JSON/TXT/TEI body只計本版原印單位。

## 追溯與形式檢查的範圍限制

正式inventory-check已執行，回傳rc=3、狀態pending：檢查414個來源盤點群組，保留142筆形式對映工作項（unexamined-category 18、present-category-without-blocks 17、undecided-block 5、single-draft-omission 48、draft-unit-not-in-inventory 54）。保守對映、多角色群組及未知來源框等限制尚未清除；這些分類不是新判定有142處漏文。prior-materials-not-excluded另有1項：盤點者製作groups時使用自己的已封存獨立raw，並非初稿；此來源關係已明列，未以隱去紀錄取得通過。原生全頁工作audit為not-run，正式pending狀態沒有改成通過。

來源處置與形式檢查分開：來源resolution共有395/395筆已完成處理決定（341筆source-reviewed-processing-resolved、54筆連結至來源未解區），另414/414實際來源block都有明確處置。所需來源讀圖未處理範圍為0，不能據此宣稱inventory形式交換或完整追溯已通過；未知來源區、形式pending及未辨明文字仍各自保留。

註記工具只比較397個共同單位，完整固定版本仍是v1的399單位與v2的398單位。共同單位追溯保留unknown-model 397與unlocated-event 36（初錄p12歷史來源未解區1＋本版目標未解區35）；新增單位另有final provenance的unknown-model 1。新增1、刪除2及拆分1另以聯集事件記錄，不以空字串偽造已錄或缺失，也不為新增單位製造初錄pointer。這些是已儲存註記的範圍與定位限制，實際原生型號／effort／tokens未知，不當0；未完成的追溯不因來源處置完成而升格。
