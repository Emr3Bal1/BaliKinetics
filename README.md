# BaliKinetics

BaliKinetics, robotik sistemler için **kinematik analiz**, **yol planlama** (RRT ve varyantları) ve **simülasyon altyapısı** sunan; 
C++ çekirdeği ve Python arayüzleri ile hem akademik araştırma hem de uygulamalı geliştirme için tasarlanmış açık kaynaklı bir projedir.

---

## 🚀 Özellikler
- İleri ve ters kinematik hesaplamaları
- Yol planlama algoritmaları: RRT, RRT*, PRM
- Simülasyon ortamı desteği (planlama → simülasyon → gerçek robot)
- C++ çekirdek + Python API
- Araştırma ve öğretim için Jupyter Notebook örnekleri
- Açık kaynaklı, katkıya açık araştırma altyapısı

---

## 📂 Klasör Yapısı
src/ → C++ çekirdek kütüphaneler
python/ → Python arayüzleri ve araçlar
notebooks/ → Deneysel çalışmalar ve görselleştirmeler
docs/ → Proje dokümantasyonu
tests/ → Birim testler

> Not: Klasörler başlangıçta boş olabilir, geliştikçe içerik eklenecektir.

## 🔧 Kurulum
```bash
# C++ derleme
mkdir -p build && cd build
cmake ..
make -j

# Python geliştirme
python -m venv .venv
source .venv/bin/activate   # Windows: .venv\Scripts\activate
pip install -e "python[dev]"

Yol Haritası

 Temel iskelet

 2D RRT demo

 İleri/ters kinematik modülleri

 Python API (pybind11)

 Simülasyon entegrasyonu

 İlk makale/rapor taslağı

 📖 Katkı

Öneriler için issue açın, PR’lar memnuniyetle kabul edilir.

📜 Lisans

Bu proje MIT lisansı ile sunulmaktadır. Ayrıntılar için LICENSE
 dosyasına bakınız.