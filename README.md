# **Anàlisi i Predicció de League of Legends**

Aquest projecte té com a objectiu analitzar dades de partides de *League of Legends* i construir un model predictiu per predir quin equip pot guanyar la partida, basant-nos en estadístiques de joc. El treball inclou una anàlisi exploratòri, pre-processament de dades, implementació de models predictius i avaluació del rendiment.

Aquest treball ha estat realitzat per: 
- Raúl Jiménez Ayza (1688916)  
- Marc Estapé Ayén (1630270)

Kaggle = https://www.kaggle.com/datasets/datasnaek/league-of-legends/data

---

## **1. Contingut del projecte**

### **1.1. Anàlisi exploratòri**
- Es va analitzar el conjunt de dades per comprendre les característiques clau i identificar relacions rellevants.
- Es van utilitzar gràfics per mostrar correlacions i patrons entre variables.
- Es van identificar atributs que aparentaven ser importants pero van resultar ser el contrari com ara:
  - La primera eliminació.
  - La primera torre destruïda.

### **1.2. Pre-processament de dades**
- Es va modificar el dataframe original per tal de millorar la qualitat d'aquest:
  - Eliminació de col·lumnes redundants com timestamp.
  - No es va trobar cap NaN ni valor poc comú, ja que totes les dades tenen el mateix tipus.
- Es va dividir el conjunt de dades en entrenament (80%) i validació/test (20%).

### **1.3. Implementació de models**
- Es van provar diversos models de classificació per predir el resultat:
  - Random Forest
  - Ada Boost
  - Gradient Boosting
- Es van ajustar els hiperparàmetres per optimitzar el rendiment amb un Grid Search.

### **1.4. Avaluació dels models**
- Es va tenir en compte la mètrica de Accuracy per seleccionar el model.
- Es van comparar els resultats entre models per seleccionar el més robust.

---

## **2. Resultats i Conclusions**
- El model de **Gradient Boost** va obtenir el millor rendiment amb una precisió superior al 90%.
- L'anàlisi va mostrar que variables com el nombre de torres destruïdes i objectius aconseguits són determinants en el resultat.
- Els resultats suggereixen que millorar el control dels objectius és clau per guanyar partides.

---

## **3. Llibreries necessàries**
Abans d'executar el projecte, assegureu-vos de tenir instal·lades les següents llibreries:
```bash
pandas
numpy
matplotlib
seaborn
scikit-learn
xgboost
