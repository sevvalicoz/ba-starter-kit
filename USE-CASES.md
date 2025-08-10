# Use Cases

## UC-01 — Sipariş Oluşturma
**Actors:** Cashier, System  
**Preconditions:** Ürünler tanımlı, kasa açık.  
**Main Flow:**
1. Cashier ürün ve adet girer.
2. İndirim oranı (varsa) girilir.
3. Ödeme yöntemi seçilir (Card/TokenFlex/Cash/POS).
4. Sistem toplamı hesaplar ve siparişi oluşturur.
5. Makbuz/çıktı üretilir.
**Alternate Flows:**
- 2a. İndirim > %20 → Sistem hata mesajı gösterir.
- 3a. Ödeme başarısız → Kullanıcı ödeme yöntemini tekrar dener.
**Postconditions:** Sipariş kaydı oluşturulmuştur.

## UC-02 — Günlük Excel Raporu Alma
**Actors:** Ops  
**Preconditions:** Gün içinde sipariş verileri mevcut.  
**Main Flow:**
1. Ops tarih aralığı seçer.
2. “Export to Excel” butonuna basar.
3. Sistem Excel dosyasını üretir ve indirir.
**Postconditions:** Excel dosyası indirildi, pivot analizine hazır.

## UC-03 — İade (Refund)
**Actors:** Finance, System  
**Preconditions:** İade politikası uygunsa, sipariş kaydı mevcut.  
**Main Flow:**
1. Finance sipariş numarasını girer.
2. Sistem uygunluğu kontrol eder.
3. İade kaydı oluşturulur; gelir negatif yazılır.
4. Raporlar güncellenir.
**Alternate Flows:**
- 2a. Uygun değil → Sistem gerekçe ile reddeder.
**Postconditions:** İade tamamlandı; finansal özet güncellendi.
