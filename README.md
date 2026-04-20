# SelfSupervised-TTT-ImageClassification
TER pour le deuxième semestre du M1 VMI.
## Contexte 
L’apprentissage auto-supervisé vise à apprendre des représentations générales à partir de grandes
quantités de données non annotées. On considérera les images dans ce projet. Ces représentations sont
ensuite spécialisées pour des tâches downstream au moyen d’un fine-tuning supervisé. Dans ce cadre, trois
ensembles de données distincts sont considérés :
1. les données non annotées utilisées lors de la phase d’auto-apprentissage,
2. les données annotées employées pour le fine-tuning supervisé,
3. les données de test, utilisées pour évaluer les performances sur les tâches downstream et,
indirectement, la qualité des représentations apprises en auto-supervision.
Toutefois, ces trois ensembles peuvent suivre des distributions différentes, ce qui entraîne un décalage de
distribution entre les phases d’auto-apprentissage, de fine-tuning et de test, et conduit à une dégradation
des performances. Le Test-Time Training (TTT) [1,2] vise à atténuer ce problème en introduisant une phase
d’adaptation au moment du test, au cours de laquelle le modèle est optimisé directement sur les données
de test, sans accès aux annotations, afin d’adapter le modèle aux conditions réelles d’inférence. Plus
précisément, le modèle d’apprentissage sera adapté individuellement à chaque image de test garantissant
une adaptation fine et locale aux variations de distribution.
## Equipe de projet et supervisor
**Étudiants**

- Maksym DOLHOV
- Fallou DIOUF
  
**Superviseurs**

- Ayoub Karine (ayoub.karine@u-paris.fr)
- Camille Kurtz (camille.kurtz@u-paris.fr)
- Laurent Wendling (Laurent.Wendling@u-paris.fr)
