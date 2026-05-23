<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0b3c95,30:1a7fbf,70:0052cc,100:00e5b0&height=220&section=header&text=Alera&fontSize=80&fontColor=ffffff&fontAlignY=40&desc=Mobil%20Güvenlik%20ve%20Davranış%20Analizi%20Platformu&descAlignY=62&descSize=22&animation=fadeIn" width="100%"/>

<br/>

[![BTU](https://img.shields.io/badge/Bursa%20Teknik%20Üniversitesi-Bilgisayar%20Mühendisliği-0b3c95?style=for-the-badge&logo=graduation-cap&logoColor=white)](https://www.btu.edu.tr)
[![Proje](https://img.shields.io/badge/Node.js%20Web%20Programlama-Dönem%20Projesi-0052cc?style=for-the-badge&logo=node.js&logoColor=white)]()
[![Durum](https://img.shields.io/badge/Durum-Geliştiriliyor-f59e0b?style=for-the-badge&logo=github-actions&logoColor=white)]()
[![Lisans](https://img.shields.io/badge/Lisans-MIT-green?style=for-the-badge&logo=opensourceinitiative&logoColor=white)]()

<br/>

> **"Giyilebilir teknolojiye gerek kalmadan, akıllı telefonunuzla görünmez bir güvenlik kalkanı."**

</div>

---

## 📋 İçindekiler

- [🛡️ Proje Hakkında](#️-proje-hakkında)
- [❗ Problem Tanımı](#-problem-tanımı)
- [🎯 Proje Amacı ve Hedefler](#-proje-amacı-ve-hedefler)
- [✨ Özellikler ve Bonuslar](#-özellikler-ve-bonuslar)
- [🗺️ Sistem Mimarisi](#️-sistem-mimarisi)
- [🛠️ Teknoloji Yığını](#️-teknoloji-yığını)
- [🧠 Yazılım Geliştirme Süreci](#-yazılım-geliştirme-süreci)
- [📅 Geliştirme Takvimi](#-geliştirme-takvimi)
- [👥 Takım ve Görev Dağılımı](#-takım-ve-görev-dağılımı)
- [🗄️ Veritabanı Tasarımı](#️-veritabanı-tasarımı)
- [⚠️ Risk Analizi](#️-risk-analizi)
- [📖 Kullanım Kılavuzu](#-kullanım-kılavuzu)
- [📦 Katkı Sağlama (Repolarımız)](#-katkı-sağlama-repolarımız)

---

## 🛡️ Proje Hakkında

**Alera**, akıllı telefonları birer IoT uç (edge) cihazı olarak kullanarak sensör verisi toplayan, bu verileri zaman serisi halinde paketleyerek (data stitching) sunucuya ileten ve gerçek zamanlı anomali tespitiyle riskli durumları yakalayan bütünsel bir **Mobil Güvenlik ve Davranış Analizi Platformudur**.

Proje kapsamında **Senaryo 2: Düşme ve Hareketsizlik Tespiti** üzerine odaklanılmış olup; yalnız yaşayan yaşlı bireyler ve tehlikeli iş kollarındaki saha çalışanları için acil durum yönetim altyapısı sunar. Sistem; **mobil uygulama (veri toplama)**, **React tabanlı web yönetim paneli (izleme)** ve **Node.js tabanlı RESTful backend API** yapısından oluşur.

```text
📱 Alera Mobil İstemci  ←→  ⚙️ Node.js API & Socket.io  ←→  🖥️ React Web Paneli
(İvmeölçer & Pil Verisi)       (Zaman Serisi & Analiz)        (Canlı Grafik/Sinyal)
                                         ↕
                                    🍃 MongoDB
```

---

## ❗ Problem Tanımı

Yalnız yaşayan yaşlı nüfusun artması ve saha çalışanlarının iş kazaları, müdahale süresinin gecikmesi nedeniyle hayati riskler barındırmaktadır:


| Sorun | Etki |
| :--- | :--- |
| 🚷 **Ani düşmeler ve bayılmalar** | Yardım çağırılamaması ve kalıcı hasar riskleri. |
| ⏳ **Uzun süreli hareketsizlik** | Sağlık krizlerinin çok geç fark edilmesi. |
| 📉 **Yüksek enerji tüketen sensörler** | Telefon bataryasının hızla tükenmesi ve sistemin kapanması. |
| 🌐 **İnternet kesintileri** | Acil durum sinyalinin merkeze zamanında ulaşamaması. |

> 👉 **Alera**; veri sıkıştırma (stitching), offline buffering ve eşik tabanlı akıllı algoritmalarıyla bu problemlere kalıcı çözümler üretir.

---

## 🎯 Proje Amacı ve Hedefler

### Temel Hedefler
* 📱 **Verimli Sensör Dinleme:** Telefonda çalışan düşük enerjili ve optimize edilmiş sensör mimarisi kurmak.
* 🔗 **Veri Sıkıştırma (Data Stitching):** İvmeölçer verilerini uç uca ekleyerek Node.js backend'e en az ağ yüküyle iletmek.
* 🧠 **Gerçek Zamanlı Analiz:** Eşik tabanlı algoritmalarla düşme tespiti yapmak ve verileri MongoDB üzerinde kalıcı saklamak.
* ⏳ **Etkileşimli Geri Sayım:** Yanlış alarmları önlemek amacıyla kullanıcı dostu ve iptal edilebilir acil durum geri sayım mekanizması geliştirmek.
* 🔐 **Rol Tabanlı Yetkilendirme:** Standart Kullanıcı ve Admin/Vasi rolleri ile veri gizliliğini en üst düzeyde korumak.
