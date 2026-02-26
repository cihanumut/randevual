## 💬 Comment İşlemleri

1. **Comment Ekleme**  (Beyza Nur Kaya)
    - **API Metodu:** `POST /comments`  
    - **Açıklama:** Müşteri, aldığı hizmet için yorum yapabilir.

2. **Comment Listeleme**  (Beyza Nur Kaya)
    - **API Metodu:** `GET /comments?businessId={businessId}`  
    - **Açıklama:** Belirli bir işletmeye ait yorumları listeler.

3. **Comment Güncelleme**  (Beyza Nur Kaya)
    - **API Metodu:** `PUT /comments/{commentId}`  
    - **Açıklama:** Müşterinin yaptığı yorumu günceller.

4. **Comment Silme**  (Beyza Nur Kaya)
    - **API Metodu:** `DELETE /comments/{commentId}`  
    - **Açıklama:** Yorumu siler.

---

## 🏢 İşletme İşlemleri

5. **İşletme Üye Olma** (Beyza Nur Kaya)  
    - **API Metodu:** `POST /businesses/register`  
    - **Açıklama:** Yeni işletme hesabı oluşturur.

6. **İşletme Giriş**  (Beyza Nur Kaya)
    - **API Metodu:** `POST /businesses/login`  
    - **Açıklama:** İşletmenin sisteme giriş yapmasını sağlar.

7. **İşletme Oluşturma**  (Beyza Nur Kaya)
    - **API Metodu:** `POST /businesses`  
    - **Açıklama:** Sisteme yeni bir işletme ekler.

8. **İşletme Güncelleme**  (Beyza Nur Kaya)
    - **API Metodu:** `PUT /businesses/{businessId}`  
    - **Açıklama:** İşletme bilgilerini günceller.

9. **İşletme Silme**  (Beyza Nur Kaya)
    - **API Metodu:** `DELETE /businesses/{businessId}`  
    - **Açıklama:** İşletmeyi sistemden kaldırır.

10. **İşletmeler Listeleme** (Beyza Nur Kaya)
    - **API Metodu:** `GET /businesses?ownerId={ownerId}`  
    - **Açıklama:** Belirli bir kullanıcıya ait tüm işletmeleri listeler.  
    - **Not:** Kendi işletmelerini listelemek için `/businesses/me` kullanılabilir.
