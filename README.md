# CoBra XP

[English Readme](https://github.com/ceteras/Cobra-Xp/blob/main/README_en.md)

CoBra XP este un design de computer bazat pe microprocesorul Z80, derivat din proiectul [Cobra](https://github.com/ceteras/CoBra).

Este construit pentru a experimenta cu circuite digitale și pentru a crea noi proiecte Z80.  
Acest lucru este făcut pentru a onora comunitatea de modderi care au muncit din greu pe computerele lor Cobra, adăugând funcții și extensii.  
Munca lor a însemnat tăierea pistelor, adăugarea de fire, construirea plăcilor de extensie și, cel mai important, cunoașterea la perfecțiune a pcb-ului și a schemei, aducând soluții inovatoare uimitoare.  
Exemple de acest tip de contribuții pot fi văzute pe [cobrasov.com](https://cobrasov.com/CoBra%20Project/index.html).  

Este de la sine înțeles că trebuie să știți ce faceți atunci când construiți Cobra XP.  
De asemenea, dacă nu aveți experiență în construirea de electronice, acest proiect poate fi o platformă serioasă de învățare pentru dvs.  

## Disclaimer:
Nu ofer garantii de nici un fel. Acesta este un experiment, alăturați-vă pe propriul risc!  
Proiectul original, la fel ca multe altele similare cu el au reputația unei anumite dificultăți în a-l face să funcționeze.  
Pentru unii dintre noi, aceasta este cea mai bună parte, după ce o construim, sesiunile de depanare pot fi spectaculoase și pot duce la o mai bună înțelegere.

## Starea experimentului
O comandă pentru un lot de plăci a fost plasată către unul dintre cei mai populari producători de pcb-uri.

![Placa de bază CoBra](https://github.com/ceteras/Cobra-Xp/blob/main/img/mainboard.png?raw=true)

## Specificații:

- CPU Z80A de 3,5 MHz
- două rânduri de cipuri DRAM cu 16 pini, pot fi instalate 4164 sau DRAM de 5V numai de 16 Kbit precum MCM4517
- trei hărți de memorie, câte una pentru fiecare: boot, modul CP/M, modul ZX Spectrum
- boot rom poate fi 27C128, 27C256, 27C512, 28C256 (28 pini)
- Rom-ul interpretor BASIC este într-un soclu cu 32 de pini, până la 4MBit 39SF040 (8x pagini de 16KB selectabile în software, încă doi jumperi pentru MSB)
- Interfață video ZX Spectrum cu rezoluție 256 x 192, adresă de bază relocabilă (modurile de pornire și CP/M plasează zona video la o adresă diferită)
- Tastatură cu 58 de taste, cu 50 de taste pentru modul ZX Spectrum plus 8 pentru CP/M
- cip de sunet AY39810
- interfață floppy i8272 - pe o placă separată (nu este inclusă în repo, pentru moment)
- Port RS232 (bit-banged)
- port joystick
- zona de prototipare, poate incapea un soclu PLCC 84 THT
- 5 amprente DIN de 28 pini 7,62 mm nepopulate, cu cipuri 26CV12 GAL de exemplu.  
fiecare dintre ele are un rând de contacte conectate la fiecare pini pentru cablare mai ușoară
- 6x headers cu 10 pini plus unul cu 4 pini pentru alimentare, conectate la magistralele de adresa și date plus câteva semnale importante de pe placă  
aceasta este menită să permită crearea de plăci de extensie.  
din păcate, nu se potrivesc cu un perfboard, nu le-am putut alinia la pasul de 0,1 inch  
un șablon pentru o placă extensie este în lucru
- 8x puncte de testare GND răspândite pe toată placa, destinate punctelor de testare cu buclă, utile pentru a agăța o clemă de masă a sondei osciloscopului
- magistralele de adrese și de date sunt, de asemenea, prezente ca puncte de testare
- jumperii smd "taie" unele conexiuni, majoritatea în partea de dos a placii, ajută la modificari, [documentația aici](https://github.com/ceteras/Cobra-Xp/blob/main/documentation/Jumpers.ods)
- port de extensie folosind un conector DIN41612 cu 3x32 pini
