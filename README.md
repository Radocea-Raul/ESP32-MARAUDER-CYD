# Cheap Yellow Marauder (CYD) - DIY Build Log

⚠️ **DISCLAIMER:** Acest dispozitiv a fost asamblat strict în scopuri educaționale. Firmware-ul ESP32 Marauder este o unealtă puternică de testare a rețelelor (pentesting). Utilizarea lui asupra rețelelor sau dispozitivelor fără consimțământul proprietarilor este ilegală.

## Despre acest build
Acest repository documentează asamblarea fizică (hardware) a unui ESP32 Marauder, folosind varianta "Cheap Yellow Display" (CYD). Deoarece proiectele hardware comerciale de acest tip pot fi destul de scumpe, am ales să urmez ruta de asamblare DIY (Do It Yourself) pentru a obține un dispozitiv cu funcționalități similare la o fracțiune din preț, având totodată și o baterie cu o capacitate mult mai mare.

Aici este rezultatul final pe care l-am obținut:

![Marauderul asamblat](poze/poza1.jpg)

![Marauderul cu ecranul jos](poze/poza2.jpg)

## Lista de Componente (Hardware)
Componentele folosite în acest proiect respectă ghidul de asamblare prezentat de canalul de YouTube HackedExistence:

* **Placa de bază:** CYD (Cheap Yellow Display) - un ESP32 cu ecran tactil integrat și cititor de carduri MicroSD (varianta cu port USB-C).
* **Baterie:** Acumulator Li-Po de 3000mAh (model 97458) pentru o durată de viață extinsă.
* **Modul GPS:** ATGM336H, echipat cu antenă ceramică, pentru funcția de wardriving și salvarea coordonatelor.
* **Încărcare:** Circuit de încărcare USB-C (1 Amp) dedicat pentru baterie.
* **Control:** Un switch slide (întrerupător) pentru a porni și opri alimentarea circuitului de la baterie.
* **Carcasă:** Carcasă printată 3D (față, spate și suport pentru stylus) fixată cu 4 șuruburi M3x6mm și inserții filetate M3.
* **Modul GPS:** Pentru funcția de wardriving (ATGM336H).
* **Card MicroSD:** Stocare.

## Firmware și Instalare
Dispozitivul rulează varianta de ESP32 Marauder portată special pentru placa CYD. 

Pentru flash-uirea firmware-ului:
1. Am folosit repository-ul menținut de **Frank Fletcher** (esp32-Marauder-cheap-yellow-display).
2. Instalarea a fost realizată direct din browser via Web Flasher (conexiune USB serială).
3. Am selectat varianta de firmware `CYD to USB` care include și suportul pentru modulul GPS.

## Funcționalități obținute
Datorită hardware-ului și firmware-ului instalat, acest dispozitiv este capabil de:
* **Wardriving:** Scanarea și cartografierea rețelelor Wi-Fi și a dispozitivelor Bluetooth folosind datele GPS.
* **Analiză Wi-Fi / Bluetooth:** Packet sniffing, deauth attacks (în rețele proprii), BLE spamming.
* **Stocare offline:** Toate capurile (PCAP) și datele capturate pot fi salvate direct pe un card MicroSD instalat în spatele ecranului.

## Credite și Resurse
Acest build nu ar fi fost posibil fără munca extraordinară depusă de comunitatea open-source:
* **[JustCallMeCoco](https://github.com/justcallmecoco/ESP32Marauder)** - Pentru crearea originală a firmware-ului fenomenal ESP32 Marauder.
* **[HackedExistence](https://www.youtube.com/watch?v=0xVrZQx4MY4)** - Pentru ghidul video detaliat și clarificarea conexiunilor hardware pentru baterie și GPS.
* **[Frank Fletcher](https://github.com/Fr4nkF13tch3r/ESP32-Marauder-Cheap-Yellow-Display)** - Pentru adaptarea codului original pe ecranele ieftine CYD.

---
*Notă: Am asamblat acest dispozitiv din pasiune pentru hardware și l-am dat mai departe unui alt pasionat, așa că acest repository servește ca jurnal al construcției mele!*
