# 🎯 Simulateur de Mouvement Parabolique

Ce projet est une application web interactive permettant de **simuler le mouvement d’un projectile** soumis à la gravité, avec ou sans résistance de l’air.  
Elle illustre les **principes de la cinématique** et de la **dynamique** d’un tir parabolique, tout en offrant une interface moderne et responsive (mobile + desktop).

---

## 🚀 Fonctionnalités principales

### 🎬 Modes de simulation
- **Mode Simulation :** visualise la trajectoire d’un projectile lancé à une vitesse et un angle donnés.  
- **Mode Cible :** détermine les angles de tir possibles pour atteindre une cible définie en coordonnées (X, Y).

### ⚙️ Paramètres configurables
Tu peux ajuster :
- La **vitesse initiale (v₀)**  
- L’**angle de tir (α)**  
- La **hauteur de départ (h_d)** et **d’arrivée (h_a)**  
- La **gravité (g)** — par exemple pour simuler la Lune ou Mars 🌕  
- La **masse du projectile (m)**  
- La **résistance de l’air**, avec :
  - le **rayon** du projectile  
  - le **coefficient de traînée (Cx)**  
  - le **modèle de frottement** : linéaire *(f ~ v)* ou quadratique *(f ~ v²)*  
  - la **forme** : sphère, cylindre, balle ou personnalisée  

### 📊 Résultats calculés
Le simulateur affiche :
- Hauteur maximale atteinte  
- Portée horizontale  
- Durée du vol  
- Vitesse à l’impact  
- Énergie mécanique initiale et à l’impact  
- Éventuelles **pertes d’énergie dues aux frottements**  

### 📈 Représentations graphiques
- Trajectoire du projectile en temps réel  
- Enveloppe théorique des tirs possibles  
- Vecteurs vitesse (avec composantes et valeurs numériques)  
- Équations analytiques de la trajectoire, vitesse et accélération (si pas de frottement)

---

## 🧠 Principes physiques

Le programme repose sur les équations du mouvement d’un projectile :
- Sans frottement :  
  \[
  y(x) = h + x \tan(\alpha) - \frac{g x^2}{2 v_0^2 \cos^2(\alpha)_
