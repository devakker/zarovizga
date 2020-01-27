# Irányítás

## Jelek/rendszerek gyorstalpaló

### Jel

A jel a fizikai mennyiség olyan értéke vagy értékváltozása, amely egy egyértelműen hozzárendelt információt hordoz. A jel tehát információtartalommal bír.

![](jelek.png)

#### Megadás

1. Képlet
2. Grafikus
3. Diffegyenlet
4. Felsorolás

### Rendszerleíró jelek

#### Egységugrásjel

![](egysegugras.png)

t=0 időpontban nem definiált!

El lehet tolni, úgy igazán hasznos:

![](tolt-egysegugras.png)

##### Ablakozás

Gyakorlatban is igen hasznos művelet. Elő tudunk állítani egy t_1 és t_2 közötti tartományon kívül 0 értékű jelet a következő módon:

![](ablak1.png)
![](ablak2.png)

#### Dirac-impulzus

Egységnyi intenzitású impulzus.

![](dirac.png)
![](dirac-def.png)

Ablakozáshoz hasonlóan lehet használni:

![](dirac-use.png)

### Általánosított derivált

x(t) általánosított deriváltja x'(t), ha fennál:

![](alt-derivalt.png)

Dirac delta integrálja:

![](dirac-egyseg.png)

..amit ha összerakunk az általánosított derivált definiciójával:

![](dirac-egyseg-derivalt.png)
## Irányítás

Egy **folyamatba** való **beavatkozás** valamely **cél** elérése érdekében.

![](iranyitas.png)

### Vezérlés - open-loop control

Az irányított jellemzőről szerzett valós idejű információ nem vesz részt az irányításban, nincs visszacsatolás.

![](vez.png)

### Szabályozás - closed-loop control

A szabályozás zárt láncú irányítás. A negatív visszacsatolást tartalmazó rendszer önműködő, zavartűrő, de a stabilitásra gondot kell fordítani.

![](szab.png)
![](alt-szab.png)

### Analóg - Digitális

![](ad-da.png)

## Sources

http://maxwell.sze.hu/JELEK/Jelek_es_rendszerek.pdf