## 📅 Randevu İşlemleri

1. **Randevu Oluşturma**
   - **API Metodu:** `POST /appointments`
   - **Açıklama:** Müşterinin seçtiği işletme ve hizmet için randevu oluşturur.

2. **Randevu Listeleme (Müşteri)**
   - **API Metodu:** `GET /appointments?customerId={customerId}`
   - **Açıklama:** Belirli bir müşteriye ait tüm randevuları listeler.  
   - **Not:** Kendi randevularını listelemek için `GET /appointments/me` kullanılabilir.

3. **Randevu Güncelleme**
   - **API Metodu:** `PUT /appointments/{appointmentId}`
   - **Açıklama:** Var olan randevunun tarih veya saat bilgilerini günceller.

4. **Randevu Silme**
   - **API Metodu:** `DELETE /appointments/{appointmentId}`
   - **Açıklama:** Randevuyu iptal eder.

---

## 🛎️ Hizmet İşlemleri

5. **Hizmet Ekleme**
   - **API Metodu:** `POST /services`
   - **Açıklama:** İşletmeye yeni hizmet ekler.

6. **Hizmet Listeleme**
   - **API Metodu:** `GET /services?businessId={businessId}`
   - **Açıklama:** Belirli bir işletmeye ait hizmetleri listeler.  
   - **Not:** Kendi işletmene ait hizmetleri listelemek için `GET /services/me` kullanılabilir.

7. **Hizmet Güncelleme**
   - **API Metodu:** `PUT /services/{serviceId}`
   - **Açıklama:** Hizmet bilgilerini günceller.

8. **Hizmet Silme**
   - **API Metodu:** `DELETE /services/{serviceId}`
   - **Açıklama:** Hizmeti kaldırır.

---

## 🗂️ Kategori İşlemleri

9. **Kategori Listeleme (ID Bazlı)**
   - **API Metodu:** `GET /categories/{categoryId}`
   - **Açıklama:** Belirli bir kategorideki işletmeleri getirir.

10. **Tüm Kategorileri Listeleme**
    - **API Metodu:** `GET /categories`
    - **Açıklama:** Sistemdeki tüm kategorileri listeler.
