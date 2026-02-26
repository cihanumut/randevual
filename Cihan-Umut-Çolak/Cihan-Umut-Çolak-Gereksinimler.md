## 👤 Müşteri İşlemleri

1. **Müşteri Üye Olma**  
   - **API Metodu:** `POST /customers/register`  
   - **Açıklama:** Yeni müşterilerin sisteme kayıt olmasını sağlar. Kullanıcı adı, email ve şifre bilgileri alınarak hesap oluşturulur.

2. **Müşteri Giriş**  
   - **API Metodu:** `POST /customers/login`  
   - **Açıklama:** Müşterinin email ve şifre ile sisteme giriş yapmasını sağlar. Başarılı girişte kimlik doğrulama için token döndürülür.

3. **Profil Görüntüleme**  
   - **API Metodu:** `GET /customers/{customerId}`  
   - **Açıklama:** Müşterinin profil bilgilerini getirir. Kullanıcı sadece kendi profilini görüntüleyebilir.  
   - **Not:** Kendi profilini görüntülemek için `/customers/me` kullanılabilir.

4. **Profil Güncelleme** 
   - **API Metodu:** `PUT /customers/{customerId}`  
   - **Açıklama:** Müşterinin profil bilgilerini güncellemesini sağlar.  
   - **Not:** Kendi profilini güncellemek için `/customers/me` kullanılabilir.

5. **Hesap Silme**  
   - **API Metodu:** `DELETE /customers/{customerId}`  
   - **Açıklama:** Müşteri hesabını kalıcı olarak siler.  
   - **Not:** Kendi hesabını silmek için `/customers/me` kullanılabilir.

---
 
## 🏢 İşletme Randevu İşlemleri

6. **İşletmeye Ait Randevuları Listeleme**  
    - **API Metodu:** `GET /appointments?businessId={businessId}`  
    - **Açıklama:** Belirli bir işletmeye ait tüm randevuları listeler.  
    - **Not:** Kendi işletmene ait randevuları listelemek için `/appointments/me` veya `/businesses/me/appointments` kullanılabilir.

--- 

## 👨💼 Çalışan İşlemleri

7. **Çalışan Ekleme**  
    - **API Metodu:** `POST /employees`  
    - **Açıklama:** İşletmeye yeni çalışan ekler.

8. **Çalışan Güncelleme**  
    - **API Metodu:** `PUT /employees/{employeeId}`  
    - **Açıklama:** Çalışan bilgilerini günceller.

9. **Çalışan Silme**  (Cihan Umut Çolak)
    - **API Metodu:** `DELETE /employees/{employeeId}`  
    - **Açıklama:** Çalışanı siler.

---
