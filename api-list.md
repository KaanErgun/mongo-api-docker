| Metot | Endpoint                             | Açıklama                                           |
|-------|--------------------------------------|----------------------------------------------------|
| POST  | /api/windsurf/auth/login             | Kullanıcı giriş işlemi                              |
| POST  | /api/windsurf/auth/register          | Yeni kullanıcı kaydı                                |
| POST  | /api/windsurf/auth/logout            | Oturumu sonlandırma                                 |
| POST  | /api/windsurf/auth/refresh           | JWT token yenileme                                  |
| POST  | /api/windsurf/auth/forgot-password   | Şifre sıfırlama isteği                             |
| POST  | /api/windsurf/auth/reset-password    | Şifre sıfırlama işlemi                             |
| GET   | /api/windsurf/users                  | Tüm kullanıcıları listele (admin yetkisi gerektirir)|
| GET   | /api/windsurf/users/{id}             | Belirli kullanıcı detayları                        |
| POST  | /api/windsurf/users                  | Yeni kullanıcı oluştur                              |
| PUT   | /api/windsurf/users/{id}             | Kullanıcı bilgilerini güncelle                      |
| DELETE| /api/windsurf/users/{id}             | Kullanıcı silme                                     |
| GET   | /api/windsurf/profile                | Giriş yapmış kullanıcının profil bilgileri          |
| PUT   | /api/windsurf/profile                | Profil güncelleme                                   |
| PUT   | /api/windsurf/profile/password       | Şifre değiştirme                                    |
| GET   | /api/windsurf/products               | Ürün (windsurf ekipmanı) listesi                    |
| GET   | /api/windsurf/products/{id}          | Ürün (ekipman) detayları                            |
| POST  | /api/windsurf/products               | Yeni ürün (ekipman) ekleme                          |
| PUT   | /api/windsurf/products/{id}          | Ürün (ekipman) güncelleme                           |
| DELETE| /api/windsurf/products/{id}          | Ürün (ekipman) silme                                |
| GET   | /api/windsurf/products/{id}/reviews  | Ürün yorumlarını listele                            |
| GET   | /api/windsurf/orders                 | Sipariş listesi                                     |
| GET   | /api/windsurf/orders/{id}            | Sipariş detayları                                   |
| POST  | /api/windsurf/orders                 | Yeni sipariş oluşturma                              |
| PUT   | /api/windsurf/orders/{id}            | Sipariş güncelleme (örn. kargo bilgisi)             |
| DELETE| /api/windsurf/orders/{id}            | Sipariş iptali                                      |
| POST  | /api/windsurf/upload                 | Dosya/resim yükleme                                 |
| GET   | /api/windsurf/files/{id}             | Dosya görüntüleme/indirme                           |
| DELETE| /api/windsurf/files/{id}             | Dosya silme                                         |
| GET   | /api/windsurf/notifications          | Bildirim listesi                                    |
| PUT   | /api/windsurf/notifications/{id}/read| Bildirimi okundu olarak işaretleme                  |
| GET   | /api/windsurf/search?q=anahtar       | Genel arama                                         |
| GET   | /api/windsurf/products?category=...  | Listeleme, filtreleme ve sıralama                   |
| GET   | /api/windsurf/dashboard              | Özet veriler (kayıt/sipariş sayısı vb.)             |
| GET   | /api/windsurf/reports/sales          | Satış raporu                                        |
