# Analiza e Rezervimeve - City Hotel

**Analiza e Rezervimeve - Hotel City**

---

## Përmbledhja

**Qëllimi i analizës:**

Kjo analizë u krye për të identifikuar faktorët kryesorë që kontribuojnë në shkallën e lartë të anulimeve të rezervimeve në Hotel City.

**Problemi kryesor i biznesit:**

Hotel City po përballet me humbje të konsiderueshme të të ardhurave për shkak të anulimeve të shumta të rezervimeve, të cilat ndikojnë në parashikimet financiare dhe menaxhimin e kapaciteteve.

**Fushat kryesore të analizës:**

- Shteti i klientëve që anulojnë më shpesh
- Lloji i depozitës dhe lidhja me anulimet
- Koha e udhëheqjes (lead time) dhe ndikimi në anulime
- Segmenti i tregut dhe kanali i shpërndarjes së rezervimeve
- Ndikimi i sezonalitetit në shkallën e anulimeve

---

## Struktura e të Dhënave

**Dataseti:**

Përdora një dataset të rezervimeve të gjetur në [Kaggle](https://www.kaggle.com/datasets/thedevastator/hotel-bookings-analysis), i cili përmbante informacione të detajuara mbi rezervimet e bëra dhe anulimet e tyre.

**Kolonat kryesore të analizës:**

- `is_canceled` – Tregon nëse rezervimi është anuluar apo jo
- `lead_time` – Ditët ndërmjet rezervimit dhe check-in-it
- `country` – Shteti i klientit
- `market_segment` – Segmenti i tregut për rezervimin
- `distribution_channel` – Kanali i shpërndarjes së rezervimit
- `deposit_type` – Lloji i depozitës (jo-rimbursueshme, nuk kërkohet depozitë, etj.)
- `agent` – Agjenti përmes të cilit është bërë rezervimi
- `company` – Kompania përmes së cilës është bërë rezervimi
- `reservation_status` – Statusi përfundimtar i rezervimit

**Përpunimi i të dhënave me SQL**

Në këtë projekt, u përdor SQL për të analizuar dataset-in, filtruar rezervimet sipas segmentit dhe gjetur modelet e anulimeve.

---

## Përmbledhje Ekzekutive

**Gjetjet kryesore:**

Përmes analizës, u identifikuan burimet kryesore të anulimeve. Rezultatet treguan se 80% e anulimeve vinin nga dy grupe kryesore të klientëve:

1. Klientët nga Portugalia që bënin rezervime vetëm për të rritur, nëpërmjet segmenteve "Groups" dhe "Online TA/TO", me zgjedhjen e vakteve vetëm mëngjes.
2. Rezervimet për të rritur nëpërmjet "Online TA", me kanal shpërndarjeje "TA/TO", dhe të bëra nga agjenti me ID 9.

---

## Thellimi i Gjetjeve

**Shteti i klientëve dhe ndikimi në anulime:**

- Shumica e anulimeve (pjesa më e madhe e 80%-shit të identifikuar) vijnë nga klientët nga Portugalia.

**Lloji i depozitës dhe shkalla e anulimeve:**

- Rezervimet me depozitë jo të rimbursueshme kanë pothuajse 100% shkallë anulimi.

**Koha e udhëheqjes dhe anulimet:**

- Sa më i lartë të jetë "lead time" (koha nga rezervimi deri në datën e qëndrimit), aq më e lartë është mundësia e anulimit.

**Segmenti i tregut dhe anulimet:**

- Segmenti "Groups" ka shkallën më të lartë të anulimeve, por segmenti "Online TA" ka më shumë anulime për shkak të volumit më të madh të rezervimeve.
    

---

## Rekomandime

**1. Optimizimi i politikave të rezervimeve për klientët nga Portugalia**

Duke qenë se shumica e anulimeve vijnë nga ky grup, hoteli duhet të analizojë më tej arsyet e anulimeve dhe të marrë masa për të reduktuar ndikimin e tyre.

**2. Përmirësimi i kushteve të depozitave**

Duke qenë se rezervimet me depozitë jo të rimbursueshme kanë shkallë të lartë anulimi, sugjerohet të rishikohen kushtet e këtyre rezervimeve ose të ofrohen stimuj për klientët që zgjedhin këtë opsion.

**3. Kufizimi i rezervimeve me "lead time" shumë të gjatë**

Duke marrë parasysh që rezervimet me një "lead time" të gjatë kanë më shumë gjasa të anulohen, mund të vendosen politika që kufizojnë rezervimet shumë afatgjata ose të ofrohen stimuj për klientët që konfirmojnë qëndrimin e tyre më herët.

**4. Rishikimi i strategjive për "Groups" dhe "Online TA"**

Pasi këto segmente përbëjnë pjesën më të madhe të anulimeve, mund të shqyrtohen mënyra alternative të menaxhimit të tyre, si rishikimi i kushteve të anulimit për këto kategori ose ofrimi i bonuseve për rezervimet e garantuara.

**5. Vlerësimi i agjentit me ID 9**

Duke qenë se rezervimet përmes këtij agjenti kanë shkallë të lartë anulimi, mund të shqyrtohet performanca e tij dhe të vendosen kushte të reja për rezervimet e bëra nëpërmjet tij.
