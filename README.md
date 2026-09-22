# [English below] Projet de Recherche Mathématiques: Modele du Tas de Sables Abelien

# Abelian Sandpile Model (Modèle du Tas de Sable Abélien)

Projet d'étude mathématique sur la dynamique, la commutativité et la géométrie de propagation du modèle du tas de sable sur $\mathbb{Z}^2$.

---

## Présentation du projet

Ce travail analyse le comportement d'un système discret de physique statistique et de combinatoire : le **modèle du tas de sable abélien** sur une grille infinie bidimensionnelle $\mathbb{Z}^2$. 

L'objectif est d'étudier la convergence, l'indépendance de l'ordre des transitions (propriété abélienne) et les propriétés géométriques de la propagation des grains.

---

## Cadre formel & Règles

### 1. Configuration (État)
Un état est une fonction $\eta : \mathbb{Z}^2 \to \mathbb{N}$, où $\eta_{i,j}$ représente le nombre de grains de sable présents au site $(i, j)$ :
- **Sommet stable :** $\eta_{i,j} \le 4$
- **Sommet instable :** $\eta_{i,j} \ge 5$ (dans le cadre de déclenchement à seuil $\ge 4$)
- **État globalement stable :** $\forall (i, j) \in \mathbb{Z}^2, \, \eta_{i,j} \le 4$

### 2. Opérateur d'avalanche
Lorsqu'un site $(i_0, j_0)$ est instable, il se décharge :
- Il perd **4 grains**.
- Il distribue **1 grain** à chacun de ses 4 voisins immédiats : $(i_0 \pm 1, j_0)$ et $(i_0, j_0 \pm 1)$.

L'opération se modélise par une matrice d'avalanche $A^{(i_0, j_0)}$ :
$$\eta' = \eta + A^{(i_0, j_0)}$$

---

## Résultats & Théorèmes Principaux

### 1. Propriété d'échange net nul
Deux sites voisins simultanément instables n'échangent aucun grain net lors de leurs décharges respectives : l'envoi mutuel de 1 grain s'annule.

### 2. Commutativité
L'addition matricielle dans $M_{\mathbb{Z}^2}(\mathbb{Z})$ étant commutative :
$$(\eta_0 + A^{x}) + A^{y} = (\eta_0 + A^{y}) + A^{x}$$

### 3. Théorème Abélien (Théorème principal)
Pour une configuration initiale donnée $\eta$ se stabilisant via deux séquences admissibles d'avalanches $(x_1, \dots, x_l)$ et $(y_1, \dots, y_{l'})$ :
- **Unicité de l'état final :** $\eta^{(1)} = \eta^{(2)}$
- **Invariant du nombre d'étapes :** $l = l'$

> **Conclusion :** Ni l'ordre dans lequel les avalanches sont déclenchées, ni le choix des sites intermédiaires n'affectent le résultat final ou la durée du processus.

---

## Géométrie et Bornes de Propagation

On note $C_n$ l'ensemble des sites de $\mathbb{Z}^2$ ayant reçu au moins un grain après $n$ avalanches, avec un nombre total de grains $G$ (invariant) :

| Propriété | Formulation mathématique | Interprétation |
| :--- | :--- | :--- |
| **Croissance** | $C_0 \subset C_1 \subset \dots \subset C_n$ | La zone visitée s'étend de manière monotone |
| **Borne de surface** | $\mathrm{Card}(C_n) \le 4n + 1$ et $\mathrm{Card}(C_n) \le G$ | Croissance au plus linéaire par rapport au temps |
| **Frontière** | $\mathrm{Card}(\partial C_n) \le G$ | Le bord est contrôlé par la masse totale |
| **Topologie** | $C_n$ est connexe par chemins | Absence d'îlots déconnectés de l'origine |
| **Confinement** | $C_n \subset [-G, G]^2$ | Propagation strictement bornée par le nombre de grains |
| **Stabilisation** | Processus fini | Atteinte obligatoire d'un état d'équilibre |
---

## Auteurs
Recherche effectuée par :
- Selima Klibi
- Romane Nouvelle
- Assiya Rakhymberdi
- Narimene Boudab

---

# [ENGLISH] Mathematics Research Project: Abelian Sandpile Model

> **Note:** The full research report and original documentation are written in French.

Mathematical research project studying the dynamics, commutativity, and propagation geometry of the abelian sandpile model on $\mathbb{Z}^2$.

---

## Project Overview

This project investigates the behavior of a discrete dynamical system from statistical physics and combinatorics: the **Abelian Sandpile Model** on an infinite two-dimensional grid $\mathbb{Z}^2$.

The key objectives are to study convergence, path independence across transition sequences (the abelian property), and the geometric properties governing grain propagation.

---

## Formal Framework & Rules

### 1. Configuration (State)
A configuration (or state) is a function $\eta : \mathbb{Z}^2 \to \mathbb{N}$, where $\eta_{i,j}$ denotes the number of sand grains at site $(i, j)$:
- **Stable site:** $\eta_{i,j} \le 4$
- **Unstable site:** $\eta_{i,j} \ge 5$ (toppling threshold defined at $\ge 4$)
- **Globally stable state:** $\forall (i, j) \in \mathbb{Z}^2, \, \eta_{i,j} \le 4$

### 2. Toppling Operator (Avalanche)
When a site $(i_0, j_0)$ becomes unstable, it topples:
- It loses **4 grains**.
- It distributes **1 grain** to each of its 4 nearest neighbors: $(i_0 \pm 1, j_0)$ and $(i_0, j_0 \pm 1)$.

This operation is modeled by a toppling matrix $A^{(i_0, j_0)}$:
$$\eta' = \eta + A^{(i_0, j_0)}$$

---

## Key Results & Theorems

### 1. Zero Net Exchange Property
Two neighboring sites that are simultaneously unstable do not exchange any net grains during their respective topplings: the mutual transfer of 1 grain cancels out.

### 2. Commutativity
Since matrix addition in $M_{\mathbb{Z}^2}(\mathbb{Z})$ is commutative:
$$(\eta_0 + A^{x}) + A^{y} = (\eta_0 + A^{y}) + A^{x}$$

### 3. Abelian Theorem (Main Theorem)
For any given initial configuration $\eta$ that stabilizes through two admissible toppling sequences $(x_1, \dots, x_l)$ and $(y_1, \dots, y_{l'})$:
- **Uniqueness of final state:** $\eta^{(1)} = \eta^{(2)}$
- **Invariance of sequence length:** $l = l'$

> **Conclusion:** Neither the order in which avalanches are triggered nor the choice of intermediate sites affects the final stable state or the total number of topplings.

---

## Propagation Geometry and Bounds

Let $C_n$ denote the set of sites in $\mathbb{Z}^2$ that have received at least one grain after $n$ topplings, with $G$ representing the total number of grains (an invariant of the system):

| Property | Mathematical Formulation | Interpretation |
| :--- | :--- | :--- |
| **Growth** | $C_0 \subset C_1 \subset \dots \subset C_n$ | The visited area expands monotonically |
| **Area Bound** | $\mathrm{Card}(C_n) \le 4n + 1$ and $\mathrm{Card}(C_n) \le G$ | Sublinear/linear spatial growth over time |
| **Boundary** | $\mathrm{Card}(\partial C_n) \le G$ | The perimeter is controlled by the total mass |
| **Topology** | $C_n$ is path-connected | No disconnected islands from the origin |
| **Confinement** | $C_n \subset [-G, G]^2$ | Spatial propagation is strictly bounded by $G$ |
| **Stabilization** | Finite process | The system is guaranteed to reach an equilibrium |

---

## Authors
Research conducted by:
- Selima Klibi
- Romane Nouvelle
- Assiya Rakhymberdi
- Narimene Boudab
