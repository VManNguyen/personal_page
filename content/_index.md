+++
title = "Informations professionnelles"
template = "page-cv.html"

+++
## Présentation
Mon domaine de recherche porte sur l'analyse à la compilation des codes de 
simulation HPC, en particulier des programmes MPI. Cela nous permet de détecter
au plus tôt des erreurs de programmation pouvant corrompre des données en raison 
d'accès concurrents aux données, ou pouvant empêcher la finition du programme.
Les résultats de cette analyse statique peuvent également nous permettre de
transformer le code à la compilation, par exemple pour dégager du potentiel de
recouvrement. 

Ma thèse, soutenue en décembre 2022, porte sur l'analyse et l'optimisation des 
appels MPI non-bloquants au sein des codes de calcul. 

Je suis désormais *ingénieur-chercheur* et *expert technique* auprès 
d'Eviden, notamment pour les thématiques relatives à MPI et aux communications 
MPI One-Sided. 

**Mots-clés** : Compilation, MPI, Analyse statique, Optimisation de code

## Encadrement
- 2023 - maintenant : Radjasouria Vinayagame, *doctorant*, avec Emmanuelle Saillard (co-directrice, Inria Bordeaux), Samuel Thibault (co-directeur, Inria Bordeaux), et Marc Sergent (co-encadrant, Eviden)

## Enseignement
- 2020 - 2023, vacataire : **Compilation avancée**, *3è année ENSIIE (équivalent M2)*. Construction d'une passe compilation GCC pour vérifier les séquences d'appels de communications collectives MPI. Manipulations du CFG et utilisation des notions de domination et post-domination d'un noeud.

## Publications
### Thèse
> [Vérification et optimisation à la compilation des communications MPI non-bloquantes](https://www.theses.fr/2022BORD0415)

> Les clusters de Calcul Haute Performance (HPC) sont composés de multiples 
unités de calcul ou de stockage mémoire, aussi appelés « nœuds », 
interconnectés par un réseau haut débit et basse latence. Une telle 
architecture est qualifiée de « distribuée ». Les calculs sont ainsi 
distribués sur ces nœuds qui vont chacun travailler sur une section d’une 
simulation, ce qui permet de réduire le temps d’exécution de simulations 
grâce au parallélisme. Les nœuds doivent toutefois se communiquer leurs 
résultats afin d’avancer dans les calculs, ce qui cause des latences. 
Message Passing Interface (MPI) est la solution la plus utilisée en HPC pour 
définir ces échanges entre nœuds de calcul. Elle définit des communications 
point-à-point et des communications collectives. Chaque type de communication 
existe en trois versions : bloquante, non-bloquante, et persistante. Les 
communications non-bloquantes permettent une meilleure utilisation des 
ressources de calcul en recouvrant les communications par des calculs, ce qui 
permet de réduire le temps d’obtention des résultats. Cependant, ces 
communications non-bloquantes sont plus complexes à l’usage, et offrent moins 
de mécanismes de sécurité. Les développeurs sont davantage susceptibles de 
commettre des erreurs de programmation pouvant conduire à des blocages du 
programme ou corrompre les résultats. Cela conduit à une moindre popularité de 
ces communications, en particulier de la forme collective introduite lors de la 
troisième révision majeure de l’interface en 2012, pour dégager du recouvrement. 
L’objectif de cette étude est de proposer des méthodes visant à aider les 
développeurs à utiliser ces communications. Premièrement, nous proposons une 
méthode pour associer les appels non-bloquants lors de la compilation d’un 
programme MPI en utilisant des informations sur le flot de contrôle et de le flot 
de données. Dans un deuxième temps, nous proposons une méthode pour 
automatiquement transformer les appels bloquants dans leur version 
non-bloquante. Cette méthode va ensuite réorganiser le code d’une fonction 
en déplaçant les dépendances des communications dans le but de maximiser 
la taille des intervalles de recouvrement. Cette méthode est également 
appliquée sur les appels non-bloquants existants en exploitant les 
associations trouvées par le processus de validation. Enfin, nous exploitons 
les limitations du processus de transformation automatique afin de proposer 
une méthode permettant d’améliorer le potentiel de recouvrement des 
programmes MPI en identifiant les bornes de ces intervalles et en suggérant 
des modifications de code à appliquer. Les trois processus que nous proposons 
ont été testés sur plusieurs benchmarks, dont des miniapps et des codes CORAL.

- Co-dirigée par Denis Barthou (Inria Bordeaux) et Patrick Carribault (CEA)
- Co-encadrée par Emmanuelle Saillard (Inria Bordeaux) et Julien Jaeger (CEA)
- Soutenue le 16 décembre 2022, à l'Université de Bordeaux

### Auteur principal
- Compas 2021 (poster), *Van Man Nguyen, Emmanuelle Saillard, Julien Jaeger, Patrick Carribault, et Denis Barthou* : **Tools for Efficient MPI Nonblocking Communications**
- [Correctness 2020](https://dx.doi.org/10.1109/Correctness51934.2020.00009), *Van Man Nguyen, Emmanuelle Saillard, Julien Jaeger, Patrick Carribault, et Denis Barthou* : **PARCOACH Extension for Static MPI Nonblocking and Persistent Communication Validation** [[hal](https://hal.science/cea-03014171v1)]
- [C3PO 2020](https://dx.doi.org/10.1007/978-3-030-59851-8_4), *Van Man Nguyen, Emmanuelle Saillard, Julien Jaeger, Patrick Carribault, et Denis Barthou* : **Automatic Code Motion to Extend MPI Nonblocking Overlap Window** [[hal](https://hal.science/cea-03010533v1)]

### Co-auteur
- [Correctness 2023](https://dx.doi.org/10.1145/3624062.3624086), *Radjasouria Vinayagame, Van Man Nguyen, Marc Sergent, Samuel Thibault, et Emmanuelle Saillard* : **Rethinking Data Race Detection in MPI-RMA Programs** [[hal](https://hal.science/hal-04272399v1)]
- [Parallel Computing 2020](https://dx.doi.org/10.1016/j.parco.2021.102859), *Joachim Protze, Marc-André Hermanns, Matthias S Müller, Van Man Nguyen, Emmanuelle Saillard, Julien Jaeger, Patrick Carribault, et Denis Barthou* : **MPI detach — Towards automatic asynchronous local completion** [[hal](https://hal.science/cea-03537990v1)]

## Contact
- email : van-man [point] nguyen [arobase] eviden [point] com
- [github](https://github.com/VManNguyen), principalement des bouts de projets personnels
