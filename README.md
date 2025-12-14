# LinkedIn İş İlanı Öneri Sistemi

### Kişiselleştirilmiş İş Önerileri Sunan Yapay Zeka Destekli Masaüstü Uygulaması

Python • Makine Öğrenmesi • Doğal Dil İşleme • PyQt5 • TF-IDF

---

## Genel Bakış

LinkedIn İş İlanı Öneri Sistemi, kullanıcıların yetkinlikleri ve iş deneyimleri doğrultusunda en uygun iş ilanlarını otomatik olarak öneren bir masaüstü uygulamasıdır.

Yüzlerce ilan arasında manuel arama yapmak yerine, kullanıcılar profil bilgilerini serbest metin olarak girer. Sistem, bu profili iş ilanlarının başlıkları, açıklamaları ve yetkinlik alanları ile karşılaştırır ve benzerlik skorlarına göre en uygun ilanları sıralar.

Uygulama tamamen yerel ortamda çalışır, CSV formatındaki LinkedIn iş ilanı verilerini kullanır ve modern bir PyQt5 grafiksel kullanıcı arayüzü sunar.

---

## Temel Özellikler

- LinkedIn iş ilanlarını CSV dosyasından yükleme  
- Yetkinlik ve deneyimler için serbest metin girişi  
- NLP tabanlı otomatik iş eşleştirme  
- Benzerlik skoruna göre sıralı iş önerileri  
- Detaylı ilan açıklama görüntüleme paneli  
- Tek tıkla ilanı tarayıcıda açma  
- Koyu temalı modern masaüstü arayüzü  

---

## Nasıl Çalışır?

1. İş ilanı başlıkları, açıklamaları ve yetkinlik alanları tek bir metin haline getirilir  
2. Metinler TF-IDF yöntemiyle sayısal vektörlere dönüştürülür  
3. Kullanıcı profil metni aynı vektörleştirme modeliyle işlenir  
4. Cosine Similarity ile profil ve ilanlar arasındaki benzerlik hesaplanır  
5. En yüksek benzerlik skoruna sahip ilk N ilan kullanıcıya önerilir  

---

## Kullanılan Teknolojiler

- Python 3.9 veya üzeri  
- PyQt5 (Masaüstü Grafiksel Arayüz)  
- pandas (CSV veri işleme)  
- scikit-learn (TF-IDF ve benzerlik hesaplama)  
- webbrowser (İlan linklerini açma)  

---

## Veri Seti Gereksinimleri

Uygulama, CSV formatındaki LinkedIn iş ilanı verileri ile çalışır.

### Zorunlu Kolonlar

title  
company_name  
description  
location  

### Opsiyonel (Önerilen) Kolonlar

skills_desc  
job_posting_url  
formatted_work_type  
formatted_experience_level  
min_salary  
max_salary  
currency  

---

## Kurulum ve Çalıştırma

### Adım 1 – Python Kurulumu

Python 3.9 veya üzeri gereklidir.

### Adım 2 – Gerekli Kütüphaneler

pip install PyQt5 pandas scikit-learn

### Adım 3 – Uygulamayı Çalıştırma

python main.py

---

## Kullanım Senaryosu

1. Uygulama başlatılır  
2. LinkedIn iş ilanı CSV dosyası seçilir  
3. Yetkinlik ve deneyimler metin olarak girilir  
4. Önerileri Getir butonuna basılır  
5. En uygun iş ilanları listelenir  
6. Seçilen ilan tarayıcıda açılır  

---

## Gelecek Çalışmalar

- FastAPI veya Flask ile web tabanlı sürüm  
- Word2Vec, BERT gibi gelişmiş NLP modelleri  
- Lokasyon ve maaş bazlı filtreleme  
- Kullanıcı geri bildirimi ile öğrenme  
- Analitik ve görselleştirme paneli  
