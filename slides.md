---
theme: default
layout: cover
class: "text-center"
highlighter: shiki
lineNumbers: false
info: |
  ## Présentation du logiciel Nelson
drawings:
  persist: false
css: unocss
---

# Logiciel Nelson

## Présentation - DATAQUITAINE 2023

### 02/03/2023

---

Intervenant: Allan CORNET

- Auteur/Développeur principal du logiciel Nelson

- Ingénieur logiciel senior EOVE (Air Liquide) Logiciels médicaux à Pau

- Auparavant :
  - ALTAIR : Ingénieur logiciel senior (développeur noyau : HyperMath Langage, Compose)
  - Scilab (INRIA) : Ingénieur logiciel senior (développeur noyau : > 7 ans)

---

# Differents type d'outils de calcul scientifitique:

Les langages de calcul scientifique permettent de résoudre des problèmes complexes en mathématiques, en ingénierie et en science, en utilisant des méthodes symboliques ou numériques.

### Calcul symbolique

- Mathematica, Maple, Maxima, ...

  Utilisés pour les calculs symboliques et la résolution de modèles mathématiques.

### Calcul numérique

- MATLAB©️, Octave, <b>Nelson</b>, SciPy, NumPy, ...

Utilisés pour les calculs numériques et la résolution de modèles mathématiques.

---

# Présentation de Nelson [1/2]

- Logiciel scientifique open source développé depuis plus de 7 ans, héritant d'un longue experience dans le domaine du calcul matriciels.

- Déjà plus 30000 téléchargement, + de 30 pays.
<div class="grid grid-cols-2">
  <div class="col-span-1">
    <img src="/images/downloads-10-02-23.png" alt="Snow" style="width:90%">
  </div>
  <div class="col-span-1">
    <img src="/images/countries.png" alt="Mountains" style="width:90%">
  </div>
</div>

---

# Présentation de Nelson [2/2]

- Particulièrement destiné aux ingénieurs, chercheurs et étudiants à la recherche des fonctions suivantes :

  - Calcul matriciel performant (Intel Math Kernel Library, Eigen3, vectorisation SIMD)
  - Calcul haute performance (OpenMP), parallele (MPI)
  - Transformée de Fourier (FFTW),
  - Interopérabilité (Fortran, C, C++, Rust)
  - Foreing Function Interface (chargement a la volée de bibliothèques dynamiques existantes)
  - Framework de tests unitaires, code coverage
  - Framework de generation de documentation
  - Création de Modules/Toolboxes externes facilité.

---

# Environnement convivial : facile à programmer

<img src="/images/Nelson-windows.png" />

---

# Méthode usuelles du calcul numérique: [1/3]

- Calcul de valeurs propres, vecteurs propres,

```matlab
A = [2, 1; 1, 2]; % input matrix

[V, D] = eig(A); % compute eigenvectors and eigenvalues

% Display the eigenvectors
disp('Eigenvectors:');
disp(V);

% Display the eigenvalues
disp('Eigenvalues:');
disp(D);
```

---

# Méthode usuelles du calcul numérique: [2/3]

- Décomposition en valeurs singulieres

```matlab
A = [1:5;4:8];
A = [A;A(1,:)+A(2,:)] %matrice de rang 2
[U, S ,V] = svd(A)
A * V
U * S
```

---

# Méthode usuelles du calcul numérique: [3/3]

- Transformée de Fourier rapide,

```matlab
N = 256; % number of samples
t = linspace(0, 2*pi, N); % time vector
x = sin(16*t) + 0.5*sin(128*t); % input signal

X = fft(x); % compute the FFT

% Plot the magnitude spectrum
figure;
plot(abs(X));
title('Magnitude Spectrum');
xlabel('Frequency (Hz)');
ylabel('Magnitude');
```

- Génération de nombres aléatoire (`rand`, `randn`, `randperm`, `rng`, ...),
- Calcul Statistiques (`corrcoef`, `cov`, `mean`, `var`, ...),
- Nombreuses primitives d'algebre linéaire (`chol`, `schur`, `det`, `rank`, `conv`, ...)

---

# Fonctions graphiques [1/2]

Tracés 2D avec des commandes de tracés de haut niveau

<div style="text-align: center;">
 <center><img width="750" src="/images/quiver.png"/></center>
</div>

---

# Fonctions graphiques [2/2]

Tracés 3D avec des commandes de tracés de haut niveau

<div style="text-align: center;">
 <center><img width="750" src="/images/colormap.png"/></center>
</div>

---

# Où trouver le logiciel Nelson ?

- **Homepage:** <https://nelson-numerical-software.github.io/nelson-website/>
- **Source code:** <https://github.com/Nelson-numerical-software/nelson>
- **Binaries:** <https://github.com/Nelson-numerical-software/nelson/releases>
- **Docker:** <https://hub.docker.com/r/nelsonsoftware/nelson/>
- **Documentation:** <https://nelson-numerical-software.github.io/nelson-website/help/en_US/>
- **GitBook:** <https://nelson-9.gitbook.io/nelson/>
- **Gitter:** <https://gitter.im/nelson-numerical-software/Lobby>
- **YouTube:** <https://www.youtube.com/channel/UCdZMnH0HC9XflNGAFFiRX9g>
- **Twitter:** <https://twitter.com/Nelson_software>

---

# NAOS - Adherent (Valorisation du logiciel Nelson)

## <img src="/images/NAOS.png" />

---

# Projets en cours avec Quantstack [1/2]

- Kernel Nelson pour Jupyterlab
    
    https://mybinder.org/v2/gh/jupyter-xeus/xeus-nelson/main?urlpath=/lab/tree/notebooks/xeus-nelson.ipynb

<div style="text-align: center;">
 <center><img width="700" src="/images/jupyterlab.png"/></center>
</div>

---

# Projets en cours avec Quantstack [2/2]

- Nelson - JupyterLite, en local dans le navigateur

  Noyau nelson , compilé en WebAssembly, s'exécute directement dans le navigateur de l'utilisateur.
  https://jupyterlite-nelson.readthedocs.io/en/latest/

<div style="text-align: center;">
 <center><img width="750" src="/images/nelson-wasm.png"/></center>
</div>

---

<div style="text-align: center;">
Objectif Version 1.0 Fin 2023  🎄 🎁 🎄 
</div>

---

# Appel aux contributeurs

<b>Dans le cadre de son développement en open source, le logiciel Nelson est à la recherche de contributeurs pour constituer une communauté et développer de nouvelles fonctionnalités.</b>

<b>Objectif:</b> intégré/partagé les codes qui seront la référence de demain.

<div style="text-align: center;">
 <center><img width= "350" src="/images/contributors.png"/></center>
</div>
---
Questions/Réponses ?
---

Merci beaucoup pour votre temps et votre attention !

contact: Allan CORNET (nelson.numerical.computation(AT)gmail.com)
