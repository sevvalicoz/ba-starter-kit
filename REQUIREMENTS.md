# Software Requirements Specification (Mini)

## 1. Purpose & Scope
Satış işlemlerinin kaydı, indirim uygulama, ödeme yöntemi seçimi (Card / TokenFlex / Cash / POS) ve günlük raporlama (Excel / BI).

## 2. Stakeholders
Business Owner, Product Manager, Finance, Ops, Dev, QA, BA.

## 3. Functional Requirements
- **FR-01**: Sipariş oluşturulabilmeli (ürün, adet, birim fiyat).
- **FR-02**: İndirim oranı uygulanabilmeli (0–0.20).
- **FR-03**: Ödeme yöntemi seçilebilmeli (Card, TokenFlex, Cash, POS).
- **FR-04**: Günlük satışlar **Excel’e** ve **Power BI**’a aktarılabilmeli.
- **FR-05**: İade işlemi negatif gelir olarak yansıtılmalı.

## 4. Non-Functional Requirements
- **NFR-01**: P95 yanıt süresi < 2 sn
- **NFR-02**: Aylık erişilebilirlik ≥ %99.5
- **NFR-03**: Log ve audit trail tutulmalı

## 5. Acceptance Criteria (örnek)
- FR-02: İndirim 0–0.20 arası; toplam = qty * unit_price * (1 - discount_rate).
