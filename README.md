# Siber Güvenlik Paneli

Bir güvenlik operasyon merkezi (SOC) için tek sayfalık izleme paneli. Kurulum gerektirmez: `index.html` dosyasını tarayıcıda açmanız yeterli.

> **Uyarı:** Paneldeki tüm rakamlar **örnek veridir**. Gerçek bir kurumun güvenlik durumunu yansıtmaz.

## İçerik

- **Özet:** Son 30 günün toplam ve kritik uyarıları, haftalık değişim, açık kritik olaylar
- **Göstergeler:** MTTD, MTTR, yama uyumu, uç nokta koruması, MFA kapsamı
- **Günlük uyarılar:** Önem derecesine göre yığılmış sütun grafik
- **Saldırı türleri:** Yatay çubuk grafik
- **Son olaylar:** Önem derecesine göre süzülebilen tablo
- **Zafiyetler:** Açık bulgular ve SLA durumu

## Veriler

Örnek veriler `veri/` klasöründe CSV olarak duruyor. Aynı veriler `index.html` içine de gömülüdür; kendi verinizi kullanmak için `index.html` içindeki `RAW` nesnesindeki CSV metinlerini değiştirin.

| Dosya | Açıklama |
| --- | --- |
| `uyarilar.csv` | Günlük uyarı sayıları (kritik, yüksek, orta, düşük) |
| `saldiri_turleri.csv` | Saldırı türüne göre olay sayısı |
| `olaylar.csv` | Olay kayıtları |
| `zafiyetler.csv` | Önem derecesine göre açık zafiyetler ve SLA |
| `gostergeler.csv` | Temel güvenlik göstergeleri, bu ve önceki dönem |

## GitHub Pages ile yayınlama

Depo ayarlarında **Settings → Pages → Branch: `main` / root** seçin. Panel birkaç dakika içinde `https://<kullanıcı-adınız>.github.io/siber-guvenlik-paneli/` adresinde açılır.

Grafikler için [d3.js](https://d3js.org) kullanılır (cdnjs üzerinden yüklenir).
