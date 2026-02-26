# Gereksinim Analizi

Aşağıda uygulamaya ait gereksinim analizi yapılıp listelenmiştir.Ekip üyeleri arasında paylaşım yapılmıştır.

# Tüm Gereksinimler 

## 👤 Müşteri İşlemleri

1. **Müşteri Üye Olma**  (Cihan Umut Çolak)
   - **API Metodu:** `POST /customers/register`  
   - **Açıklama:** Yeni müşterilerin sisteme kayıt olmasını sağlar. Kullanıcı adı, email ve şifre bilgileri alınarak hesap oluşturulur.

2. **Müşteri Giriş**  (Cihan Umut Çolak)
   - **API Metodu:** `POST /customers/login`  
   - **Açıklama:** Müşterinin email ve şifre ile sisteme giriş yapmasını sağlar. Başarılı girişte kimlik doğrulama için token döndürülür.

3. **Profil Görüntüleme**  (Cihan Umut Çolak)
   - **API Metodu:** `GET /customers/{customerId}`  
   - **Açıklama:** Müşterinin profil bilgilerini getirir. Kullanıcı sadece kendi profilini görüntüleyebilir.  
   - **Not:** Kendi profilini görüntülemek için `/customers/me` kullanılabilir.

4. **Profil Güncelleme**  (Cihan Umut Çolak)
   - **API Metodu:** `PUT /customers/{customerId}`  
   - **Açıklama:** Müşterinin profil bilgilerini güncellemesini sağlar.  
   - **Not:** Kendi profilini güncellemek için `/customers/me` kullanılabilir.

5. **Hesap Silme**  (Cihan Umut Çolak)
   - **API Metodu:** `DELETE /customers/{customerId}`  
   - **Açıklama:** Müşteri hesabını kalıcı olarak siler.  
   - **Not:** Kendi hesabını silmek için `/customers/me` kullanılabilir.

---

## 📅 Randevu İşlemleri

6. **Randevu Oluşturma**  (Melike Ünlü)
   - **API Metodu:** `POST /appointments`  
   - **Açıklama:** Müşterinin seçtiği işletme ve hizmet için randevu oluşturur.

7. **Randevu Listeleme (Müşteri)**  (Melike Ünlü)
   - **API Metodu:** `GET /appointments?customerId={customerId}`  
   - **Açıklama:** Belirli bir müşteriye ait tüm randevuları listeler.  
   - **Not:** Kendi randevularını listelemek için `/appointments/me` kullanılabilir.

8. **Randevu Güncelleme**  (Melike Ünlü)
   - **API Metodu:** `PUT /appointments/{appointmentId}`  
   - **Açıklama:** Var olan randevunun tarih veya saat bilgilerini günceller.

9. **Randevu Silme**  (Melike Ünlü)
   - **API Metodu:** `DELETE /appointments/{appointmentId}`  
   - **Açıklama:** Randevuyu iptal eder.

---

## 💬 Comment İşlemleri

10. **Comment Ekleme**  (Beyza Nur Kaya)
    - **API Metodu:** `POST /comments`  
    - **Açıklama:** Müşteri, aldığı hizmet için yorum yapabilir.

11. **Comment Listeleme**  (Beyza Nur Kaya)
    - **API Metodu:** `GET /comments?businessId={businessId}`  
    - **Açıklama:** Belirli bir işletmeye ait yorumları listeler.

12. **Comment Güncelleme**  (Beyza Nur Kaya)
    - **API Metodu:** `PUT /comments/{commentId}`  
    - **Açıklama:** Müşterinin yaptığı yorumu günceller.

13. **Comment Silme**  (Beyza Nur Kaya)
    - **API Metodu:** `DELETE /comments/{commentId}`  
    - **Açıklama:** Yorumu siler.

---

## 🏢 İşletme İşlemleri

14. **İşletme Üye Olma** (Beyza Nur Kaya)  
    - **API Metodu:** `POST /businesses/register`  
    - **Açıklama:** Yeni işletme hesabı oluşturur.

15. **İşletme Giriş**  (Beyza Nur Kaya)
    - **API Metodu:** `POST /businesses/login`  
    - **Açıklama:** İşletmenin sisteme giriş yapmasını sağlar.

16. **İşletme Oluşturma**  (Beyza Nur Kaya)
    - **API Metodu:** `POST /businesses`  
    - **Açıklama:** Sisteme yeni bir işletme ekler.

17. **İşletme Güncelleme**  (Beyza Nur Kaya)
    - **API Metodu:** `PUT /businesses/{businessId}`  
    - **Açıklama:** İşletme bilgilerini günceller.

18. **İşletme Silme**  (Beyza Nur Kaya)
    - **API Metodu:** `DELETE /businesses/{businessId}`  
    - **Açıklama:** İşletmeyi sistemden kaldırır.

19. **İşletmeler Listeleme** (Beyza Nur Kaya)
    - **API Metodu:** `GET /businesses?ownerId={ownerId}`  
    - **Açıklama:** Belirli bir kullanıcıya ait tüm işletmeleri listeler.  
    - **Not:** Kendi işletmelerini listelemek için `/businesses/me` kullanılabilir.

---

## 🏢 İşletme Randevu İşlemleri

20. **İşletmeye Ait Randevuları Listeleme**  (Cihan Umut Çolak)
    - **API Metodu:** `GET /appointments?businessId={businessId}`  
    - **Açıklama:** Belirli bir işletmeye ait tüm randevuları listeler.  
    - **Not:** Kendi işletmene ait randevuları listelemek için `/appointments/me` veya `/businesses/me/appointments` kullanılabilir.

---

## 🛎️ Hizmet İşlemleri

21. **Hizmet Ekleme**  (Melike Ünlü)
    - **API Metodu:** `POST /services`  
    - **Açıklama:** İşletmeye yeni hizmet ekler.

22. **Hizmet Listeleme**  (Melike Ünlü)
    - **API Metodu:** `GET /services?businessId={businessId}`  
    - **Açıklama:** Belirli bir işletmeye ait hizmetleri listeler.  
    - **Not:** Kendi işletmene ait hizmetleri listelemek için `/services/me` kullanılabilir.

23. **Hizmet Güncelleme**  (Melike Ünlü)
    - **API Metodu:** `PUT /services/{serviceId}`  
    - **Açıklama:** Hizmet bilgilerini günceller.

24. **Hizmet Silme**  (Melike Ünlü)
    - **API Metodu:** `DELETE /services/{serviceId}`  
    - **Açıklama:** Hizmeti kaldırır.

---

## 👨‍💼 Çalışan İşlemleri

25. **Çalışan Ekleme**  (Cihan Umut Çolak)
    - **API Metodu:** `POST /employees`  
    - **Açıklama:** İşletmeye yeni çalışan ekler.

26. **Çalışan Güncelleme**  (Cihan Umut Çolak)
    - **API Metodu:** `PUT /employees/{employeeId}`  
    - **Açıklama:** Çalışan bilgilerini günceller.

27. **Çalışan Silme**  (Cihan Umut Çolak)
    - **API Metodu:** `DELETE /employees/{employeeId}`  
    - **Açıklama:** Çalışanı siler.

---

## 🗂️ Kategori İşlemleri

28. **Kategori Listeleme (ID Bazlı)**  (Melike Ünlü)
    - **API Metodu:** `GET /categories/{categoryId}`  
    - **Açıklama:** Belirli bir kategorideki işletmeleri getirir.  

29. **Tüm Kategorileri Listeleme**  (Melike Ünlü)
    - **API Metodu:** `GET /categories`  
    - **Açıklama:** Sistemdeki tüm kategorileri listeler.

# Gereksinim Dağılımları
1. [Cihan Umut Çolak'ın Gereksinimleri](Cihan-Umut-Çolak/Cihan-Umut-Çolak-Gereksinimler.md)
2. [Beyza Nur Kaya'nın Gereksinimleri](Beyza-Nur-Kaya/Beyza-NurKaya-Gereksinimler.md)
3. [Melike Ünlü'nün Gereksinimleri](Melike-Ünlü/Melike-Ünlü-Gereksinimler.md)

