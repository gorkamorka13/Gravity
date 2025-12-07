***

# 🚀 Simulateur de Mouvement Parabolique Universel

Une application web interactive et autonome pour simuler la physique balistique. Ce projet permet non seulement d'étudier le mouvement sur Terre avec frottements, mais offre également **un comparateur multi-planétaire unique** pour visualiser simultanément les différences de gravité à travers le système solaire.

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/Vanilla%20JS-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)

## 🌌 Système Solaire et Gravité

L'un des points forts de ce simulateur est sa base de données astronomique intégrée. Vous pouvez simuler un tir n'importe où dans le système solaire.

### 1. Mode Comparaison Multi-Planétaire (Nouveau ⭐)
Visualisez **simultanément** la trajectoire d'un même projectile sur plusieurs astres. Cochez simplement les planètes souhaitées (ex: Terre vs Lune vs Jupiter) et le graphique superposera les courbes en temps réel pour une comparaison directe.

### 2. Données Gravitationnelles Intégrées
Le simulateur inclut les constantes de gravité ($g$) précises pour les corps célestes suivants :

| Astre | Gravité ($m/s^2$) |
| :--- | :--- |
| **Terre** | $9.81$ |
| **Lune** | $1.62$ |
| **Mars** | $3.71$ |
| **Mercure** | $3.70$ |
| **Vénus** | $8.87$ |
| **Uranus** | $8.69$ |
| **Saturne** | $10.44$ |
| **Neptune** | $11.15$ |
| **Jupiter** | $24.79$ |

---

## 📋 Fonctionnalités Détaillées

### 🎯 Modes de Tir
1.  **Simulation Libre :**
    *   Contrôle total des paramètres initiaux : Vitesse ($v_0$), Angle ($\alpha$), Hauteur de départ ($h$), Hauteur d'arrivée.
    *   Affichage en temps réel de la parabole.
2.  **Mode Cible (Target Challenge) :**
    *   Définissez une position cible $(x, y)$.
    *   Le moteur physique résout l'équation quadratique pour trouver **les deux angles possibles** (tir tendu et tir en cloche) permettant d'atteindre la cible avec la vitesse donnée.

### 🌬️ Physique Avancée & Aérodynamisme
Contrairement aux simulateurs basiques, celui-ci intègre un moteur physique complet pour la résistance de l'air :
*   **Modèles de Trainée :**
    *   Lineaire ($f \propto v$) : Pour les basses vitesses ou particules fines.
    *   Quadratique ($f \propto v^2$) : Pour les objets macroscopiques standards.
*   **Paramètres du Projectile :**
    *   Formes pré-configurées : Sphère ($C_x \approx 0.47$), Balle ($C_x \approx 0.295$), Cylindre.
    *   Personnalisation complète : Masse, Rayon, et $C_x$ manuel.
    *   Densité de l'air configurable.

### 📊 Analyse de Données
*   **Vecteurs Dynamiques :** Affichage des vecteurs vitesse ($\vec{v}$) et de leurs composantes ($v_x, v_y$) à chaque instant $t$.
*   **Enveloppe de Sûreté :** Tracé en pointillés de la zone maximale atteignable par le projectile (parabole de sûreté).
*   **Bilan Énergétique :** Calcul en direct de :
    *   Énergie Cinétique ($E_c$)
    *   Énergie Potentielle de pesanteur ($E_p$)
    *   Pertes dues aux frottements (en Joules).
*   **Équations Mathématiques :** Génération et affichage dynamique de l'équation de la trajectoire $y(x)$ basée sur les paramètres actuels.

---

## 🎮 Contrôles & Gestes

L'interface a été conçue pour être réactive et accessible via plusieurs méthodes d'entrée :

*   **👆 Swipe Tactile (Mobile/Tablette) :**
    *   Un glissement latéral (Swipe) permet d'ouvrir ou de fermer rapidement le panneau de configuration sans chercher le bouton.
*   **🖱️ Drag & Drop (Souris) :**
    *   En *Mode Cible*, vous pouvez cliquer et glisser la cible rouge directement sur le graphique pour changer ses coordonnées $(x, y)$ intuitivement.
*   **⌨️ Navigation Clavier :**
    *   L'interface supporte la navigation native : utilisez `Tab` pour naviguer entre les champs et `Espace` ou `Entrée` pour activer les boutons/checkboxes.

---

## 🛠 Installation

Aucune installation complexe requise. Ce projet est "Zero-Dependency".

1.  Clonez le dépôt :
    ```bash
    git clone https://github.com/votre-username/simulateur-parabolique.git
    ```
2.  Ouvrez simplement le fichier `index.html` dans votre navigateur.

---

## 📐 Aperçu Technique

Le projet repose sur une boucle d'animation (`requestAnimationFrame`) et deux méthodes de calcul :

### 1. Méthode Analytique (Sans frottement)
Utilisée pour les calculs instantanés et le tracé des enveloppes :
$$y(x) = -\frac{g}{2v_0^2 \cos^2(\alpha)} x^2 + \tan(\alpha)x + h$$

### 2. Méthode Numérique d'Euler (Avec frottement)
Utilisée lorsque la résistance de l'air est activée. La simulation itère tous les $16ms$ ($dt$) pour recalculer les vecteurs vitesse et position en fonction des forces appliquées (Gravité + Trainée).

---

## 👤 Auteur

**Michel ESPARSA**
*   Développement : 07/12/2025

## 📄 Licence

Projet libre de droits pour usage éducatif et personnel.
