# 🤖 Mini Sumo Robot

17. MEB Robot Yarışması mini sumo kategorisi için özel olarak tasarlanmış ve geliştirilmiş otonom robot projesi.

*(Not: Projenin kaynak kodları yarışma dönemine ait eski bilgisayarımda kaldığı için, bu depoda robotun donanım mimarisi, sensör mantığı ve algoritma yapısı sunulmuştur.)*

## 🎯 Projenin Amacı
Belirlenen ring (dohyo) sınırları içerisinde kalarak, otonom bir şekilde rakip robotu algılamak ve ring dışına itmek. Hız, manevra kabiliyeti ve doğru sensör okuması projenin temel odak noktalarıdır.

## 🛠️ Kullanılan Teknolojiler ve Donanımlar
* **Kontrolcü:** Arduino Nano (Küçük boyutu ve hafifliği nedeniyle tercih edildi)
* **Algılama (Rakip):** Cisimden yansımalı sensörler (Rakibi hızlı tespit etmek için)
* **Algılama (Zemin):** Çizgi izleyen / Kontrast sensörleri (Ringin beyaz sınır çizgisini algılayıp dışarı çıkmamak için)
* **Hareket:** Yüksek torklu DC motorlar ve motor sürücü kartı

## ⚙️ Savaş ve Hareket Algoritması
1. **Saldırı Modu:** Rakip sensörler tarafından algılandığı an, robot tam güçle ileri atılır ve rakibi itmeye başlar.
2. **Savunma Modu:** Zemin sensörleri ringin sınır çizgisini (beyaz çizgiyi) algıladığında, robot dışarı düşmemek için motorları aniden ters yönde çalıştırarak geri manevra yapar.
