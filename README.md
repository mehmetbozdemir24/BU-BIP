# BU-BİP

[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
[![Python](https://img.shields.io/badge/python-3.8+-blue.svg)](https://www.python.org/downloads/)
[![Status](https://img.shields.io/badge/status-in%20development-yellow.svg)]()

> RAG (Retrieval-Augmented Generation) tabanlı akıllı bilgi platformu

## 📋 Proje Özeti

Türkçe doğal dil işleme ve RAG teknolojilerini kullanan akıllı bir bilgi platformu projesidir. Kullanıcılara hızlı, doğru ve bağlam farkında yanıtlar sunmayı hedeflemektedir.

**Proje Süresi:** 12 Ay

## 🎯 Hedefler

- Türkçe dilinde optimize edilmiş dil modeli geliştirme
- Yüksek performanslı RAG sistemi kurulumu
- Kullanıcı dostu web arayüzü tasarımı
- Düşük halüsinasyon oranı ile güvenilir bilgi sunumu
- Ölçeklenebilir ve sürdürülebilir sistem mimarisi

## 🏗️ Proje Yapısı

```
BU-BIP/
├── data/                      # Veri toplama ve ön işleme
│   ├── raw/                   # Ham veriler
│   ├── processed/             # İşlenmiş veriler
│   └── scripts/               # Veri toplama scriptleri
├── models/                    # Model dosyaları
│   ├── fine-tuned/           # Fine-tune edilmiş modeller
│   └── checkpoints/          # Model checkpoint'leri
├── rag-system/               # RAG sistem bileşenleri
│   ├── embeddings/           # Embedding modelleri
│   ├── vector-db/            # Vektör veritabanı
│   └── retrieval/            # Retrieval mekanizmaları
├── api/                      # Backend API
│   ├── routes/               # API endpoint'leri
│   └── services/             # İş mantığı servisleri
├── frontend/                 # Web arayüzü
│   ├── src/                  # Kaynak kodları
│   └── public/               # Statik dosyalar
├── tests/                    # Test dosyaları
├── docs/                     # Dokümantasyon
└── configs/                  # Yapılandırma dosyaları
```

## 👥 Proje Ekibi

### Proje Yönetimi
- **Proje Yürütücüsü**
  - Akademik rehberlik
  - Metodolojik danışmanlık
  - Süreç yönetimi

### Araştırma Ekibi

| İsim | Rol | Sorumluluk Alanları |
|------|-----|---------------------|
| **Tufan Y. Çiftçioğlu** | Kıdemli Araştırmacı | İP-1 Paket Sorumlusu, İP-4 Araştırmacı |
| **Engin Demir** | Araştırmacı | İP-1 Araştırmacı, İP-4 Paket Sorumlusu |
| **Süleyman Var** | Araştırmacı | İP-2 Paket Sorumlusu |
| **Mehmet Bozdemir** | Araştırmacı | İP-3 Paket Sorumlusu |

## 📦 İş Paketleri ve Görev Dağılımı

### İP-1: Veri Toplama ve Ön İşleme
**Süre:** Ay 1–3  
**Sorumlular:** Tufan Y. Çiftçioğlu (Paket Sorumlusu), Engin Demir (Araştırmacı)

**Görevler:**
- Web scraping sistemlerinin geliştirilmesi
- Veri temizleme ve normalizasyon
- Veri kalite kontrolü ve validasyon

**Başarı Ölçütleri:**
- Minimum 100 sayfa veri toplama
- %95 doğruluk oranı
- %90 tekrar temizliği

**Risk Yönetimi:**
- **Risk:** Web sitesi yapısı değişikliği
- **B Planı:** Adaptif scraping, Vision-LLM tabanlı ayrıştırıcılar, CMS API entegrasyonu

---

### İP-2: Dil Modelinin İnce Ayarı (Fine-tuning)
**Süre:** Ay 2–6  
**Sorumlular:** Süleyman Var (Paket Sorumlusu), Proje Yürütücüsü (Akademik Danışman)

**Görevler:**
- Türkçe dil modelinin seçimi ve hazırlanması
- LoRA/QLoRA ile parametre-verimli fine-tuning
- Model değerlendirme ve optimizasyon

**Başarı Ölçütleri:**
- Perplexity %30 iyileşme
- F1 Score > 0.85
- Türkçe testlerde yüksek başarı

**Risk Yönetimi:**
- **Risk:** GPU kaynak yetersizliği
- **B Planı:** LoRA/QLoRA kullanımı, model distilasyonu, bulut GPU kiralama (Colab Pro+)

---

### İP-3: RAG Sisteminin Geliştirilmesi
**Süre:** Ay 4–7  
**Sorumlular:** Mehmet Bozdemir (Paket Sorumlusu), Proje Yürütücüsü (Akademik Danışman)

**Görevler:**
- Vektör veritabanı kurulumu (Qdrant/Pinecone/Weaviate)
- Embedding modeli entegrasyonu
- Retrieval ve re-ranking mekanizmalarının geliştirilmesi

**Başarı Ölçütleri:**
- %80 relevance (Top-5)
- Retrieval latency < 200ms

**Risk Yönetimi:**
- **Risk:** Vektör DB performans sorunları
- **B Planı:** Pinecone/Weaviate alternatifleri, hibrit arama

---

### İP-4: Sistem Entegrasyonu ve Arayüz Geliştirme
**Süre:** Ay 6–10  
**Sorumlular:** Engin Demir (Paket Sorumlusu), Tufan Y. Çiftçioğlu (Araştırmacı)

**Görevler:**
- Backend API geliştirilmesi (FastAPI/Flask)
- Frontend arayüz tasarımı (React/Vue.js)
- Sistem entegrasyonu ve deployment

**Başarı Ölçütleri:**
- API yanıt süresi < 2 saniye
- 50 eş zamanlı kullanıcı desteği
- UX skoru > 4.0/5.0

**Risk Yönetimi:**
- **Risk:** Tarayıcı/cihaz uyumsuzluğu
- **B Planı:** PWA yaklaşımı, çoklu tarayıcı desteği

---

### İP-5: Test, Değerlendirme ve İyileştirme
**Süre:** Ay 9–12  
**Sorumlular:** Tüm Ekip (Proje Yürütücüsü gözetiminde)

**Görevler:**
- Kapsamlı sistem testleri
- Kullanıcı kabul testleri (UAT)
- Performans optimizasyonu
- Dokümantasyon tamamlama

**Başarı Ölçütleri:**
- Exact Match (EM) > %75
- F1 Score > %85
- Halüsinasyon oranı < %5
- System Usability Scale (SUS) > 80/100

**Risk Yönetimi:**
- **Risk:** Halüsinasyon oranı yüksek
- **B Planı:** Güven skoru eşik değerleri, kaynak kısıtlama, insan denetimli doğrulama

## 🛠️ Teknoloji Yığını

### Backend
- Python 3.8+
- FastAPI / Flask
- LangChain / LlamaIndex
- Transformers (Hugging Face)

### Dil Modelleri
- Fine-tuned Turkish LLM
- LoRA/QLoRA için PEFT
- Gemma / LLaMA adaptasyonları

### RAG & Vektör DB
- Qdrant / Pinecone / Weaviate
- Sentence Transformers
- Turkish embedding modelleri

### Frontend
- React / Vue.js / Streamlit
- Progressive Web App (PWA)
- Responsive tasarım

### DevOps
- Docker & Docker Compose
- Git & GitHub
- CI/CD pipeline

## 🚀 Kurulum

### Gereksinimler
```bash
Python >= 3.8
CUDA >= 11.8 (GPU kullanımı için)
Docker (opsiyonel)
```

### Adımlar

1. **Repository'yi klonlayın**
```bash
git clone https://github.com/[kullanici-adi]/BU-BIP.git
cd BU-BIP
```

2. **Sanal ortam oluşturun**
```bash
python -m venv venv
source venv/bin/activate  # Linux/Mac
# veya
venv\Scripts\activate  # Windows
```

3. **Bağımlılıkları yükleyin**
```bash
pip install -r requirements.txt
```

4. **Yapılandırma dosyasını ayarlayın**
```bash
cp configs/config.example.yaml configs/config.yaml
# config.yaml dosyasını düzenleyin
```

5. **Vektör veritabanını başlatın**
```bash
docker-compose up -d vector-db
```

6. **Uygulamayı çalıştırın**
```bash
python main.py
```

## 📊 Başarı Metrikleri

| Metrik | Hedef | Mevcut Durum |
|--------|-------|--------------|
| Veri Toplama | 100+ sayfa | 🔄 İşlemde |
| Veri Doğruluğu | %95 | 🔄 İşlemde |
| Model Perplexity İyileşmesi | %30 | 🔄 İşlemde |
| F1 Score | > 0.85 | 🔄 İşlemde |
| RAG Relevance (Top-5) | %80 | 🔄 İşlemde |
| Retrieval Latency | < 200ms | 🔄 İşlemde |
| API Yanıt Süresi | < 2 sn | 🔄 İşlemde |
| Eş Zamanlı Kullanıcı | 50 | 🔄 İşlemde |
| Halüsinasyon Oranı | < %5 | 🔄 İşlemde |
| SUS Skoru | > 80/100 | 🔄 İşlemde |

## 📅 Proje Zaman Çizelgesi

```
Ay 1-3:   ████████░░░░░░░░░░░░░░░░ İP-1: Veri Toplama
Ay 2-6:   ░░██████████████░░░░░░░░ İP-2: Model Fine-tuning
Ay 4-7:   ░░░░░░████████████░░░░░░ İP-3: RAG Geliştirme
Ay 6-10:  ░░░░░░░░░░████████████░░ İP-4: Entegrasyon
Ay 9-12:  ░░░░░░░░░░░░░░░░████████ İP-5: Test & İyileştirme
```

## 🤝 Katkıda Bulunma

Proje ekibi içi katkılar için:

1. Yeni bir branch oluşturun (`git checkout -b feature/YeniOzellik`)
2. Değişikliklerinizi commit edin (`git commit -m 'Yeni özellik eklendi'`)
3. Branch'inizi push edin (`git push origin feature/YeniOzellik`)
4. Pull Request oluşturun

## 📝 Lisans

Bu proje [MIT Lisansı](LICENSE) altında lisanslanmıştır.

## 📧 İletişim

**Proje Yürütücüsü:** [Akademik Danışman]  
**Ekip İletişim:** GitHub Issues üzerinden

---

## 🔗 Kaynaklar

- [LangChain Dokümantasyonu](https://python.langchain.com/)
- [Hugging Face Transformers](https://huggingface.co/docs/transformers)
- [Qdrant Vector Database](https://qdrant.tech/documentation/)
- [FastAPI Dokümantasyonu](https://fastapi.tiangolo.com/)

---

**Not:** Bu proje aktif geliştirme aşamasındadır. Güncellemeler için repository'yi takip edin.
