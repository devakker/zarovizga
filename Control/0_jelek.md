# Jelek/rendszerek gyorstalpaló

## Jel

A jel a fizikai mennyiség olyan értéke vagy értékváltozása, amely egy egyértelműen hozzárendelt információt hordoz. A jel tehát információtartalommal bír.

![](jelek.png)

### Megadás

1. Képlet
2. Grafikus
3. Diffegyenlet / Rekurziv formula
4. Felsorolás

## Rendszerleíró jelek

### Egységugrásjel

![](egysegugras.png)

t=0 időpontban nem definiált!

El lehet tolni, úgy igazán hasznos:

![](tolt-egysegugras.png)

#### Ablakozás

Gyakorlatban is igen hasznos művelet. Elő tudunk állítani egy t_1 és t_2 közötti tartományon kívül 0 értékű jelet a következő módon:

![](ablak1.png)
![](ablak2.png)

### Dirac-impulzus

Egységnyi intenzitású impulzus.

![](dirac.png)
![](dirac-def.png)
![](dirac-egyseg-def.png)

Ablakozáshoz hasonlóan lehet használni:

![](dirac-use.png)

### Általánosított derivált

x(t) általánosított deriváltja x'(t), ha fennál:

![](alt-derivalt.png)

Dirac delta integrálja:

![](dirac-egyseg.png)

..amit ha összerakunk az általánosított derivált definiciójával:

![](dirac-egyseg-derivalt.png)

### Jelek további osztályozása

* Sztochasztikus - determinisztikus
* Páros - páratlan
* Korlátos
* ...

## Rendszer

![](rendszer.png)

A rendszer egy fizikai objektum valamilyen modellje amely matematikailag leírja annak működését. Lehet SISO vagy MIMO.

Fontos tulajdonságok:

### Lineáris

a rendszerre érvényes a szuperpozíció elve, W operátor lineáris.

![](linren.png)

### Invariáns

A gerjesztés időbeli eltolása azt eredményezi, hogy a válaszban csak egy ugyanekkora időbeli eltolódás következik be:

![](invarren.png)

### Kauzális

A rendszer válaszának adott időpontbeli értéke nem függ a gerjesztés jövőbeli értékétől.

### GV-stabil

Bármely korlátos gerjesztésre korlátos választ ad. (bibo)

## Válasz összetevők

![](2020-01-30-00-51-07.png)