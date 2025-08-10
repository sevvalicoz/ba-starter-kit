# User Stories (INVEST)

- **US-01**: (Cashier) Ürün ve adedi girerek **sipariş oluşturmak** istiyorum ki satış kaydı oluşsun.
  - **AC**: Zorunlu alanlar (ürün, adet, fiyat, ödeme yöntemi) dolmadan kayıt yapılamaz.

- **US-02**: (User) Siparişte **indirim uygulamak** istiyorum ki kampanya yansısın.
  - **AC**: İndirim aralığı %0–%20; toplam = qty * unit_price * (1 - discount_rate).

- **US-03**: (Ops) **Günlük satış raporunu Excel’e** almak istiyorum ki operasyon raporları üretim kolay olsun.
  - **AC**: Tarih, şehir, ödeme yöntemi, gelir kolonları bulunur; dosya indirilebilir.

- **US-04**: (Finance) **İade işlemi** yapmak istiyorum ki hatalı satışlar düzelsin.
  - **AC**: İade geliri negatif yazar; ilgili siparişe bağlanır; raporlara yansır.

- **US-05**: (PM) Ödeme yöntemlerine göre **KPI dashboard** görmek istiyorum ki iş kararları kolaylaşsın.
  - **AC**: Toplam gelir, AOV, refund oranı ve TokenFlex payı ayrı kartlarda görünür.

- **US-06**: (BA) **Gereksinim–test izlenebilirliği** görmek istiyorum ki kapsam kontrol edilsin.
  - **AC**: RTM’de FR/NFR → US → Test Case eşleşmeleri listelenir.
