# Logistic-regression-for-Transport-choice-in-SAS
Logistic Modeling for choosing a particular mean of transport using SAS base programming



Pour transporter une personne d'un point à un autre, il est possible d'utiliser successivement plusieurs modes de transport. Les raisons de coût, de rapidité et de sécurité guident le choix des modes de transport qui seront mis en œuvre. Quelques fois, c'est la géographie, le climat et plus généralement l'environnement qui obligent à utiliser un mode de transport plutôt qu'un autre.
Face à différents avantages et inconvénients, un agent rationnel choisira l'option qui maximise le plus son utilité.
**Dans ce rapport, il s’agira d’étudier  le comportement de 152 ménages face à trois choix de mode de transport pour leurs vacances.** Nous choisissons de modéliser un logit multinomial non-ordonné.
En effet, le modèle logit polytomique non ordonné, introduit par Mc Fadden en 1968 constitue une famille de modèles économétriques adaptés au cas  où la variable à expliquer est une variable qualitative, dont les  modalités ne peuvent être classées les unes par rapport aux autres.

Nous allons au cours de cette étude déterminer les préférences quant aux modes de transports utilisés par les 152 ménages de notre base de données, afin de partir en vacances. 
Le choix pour la population étudiée se limite à 3 alternatives : **le bus, le train et la voiture.**
Les variables constituant le modèle sont : 

 - ttrajet mesure le temps de trajet
 - tgare mesure le temps passé en gare (0 pour la voiture)
 - ttotal mesure la durée totale du voyage ((ttotal = tgare + ttrajet)
  - ctrajet mesure le coût du trajet
 - ctotal mesure le coût total du voyage
 - revm mesure le revenu du ménage
 - npers mesure le nombre de personnes voyageant dans le groupe.
 
Nous verrons dans un premier temps grâce au test d’Hausmann si **l’hypothèse d’indépendance des alternatives non pertinentes** est respectée ou pas. Si cette hypothèse est respectée, nous choisirons alors pour notre étude un modèle logit conditionnel. Si elle n’est pas respectée, nous devrons utiliser un modèle logit emboité.
 Nous analyserons ensuite les résultats obtenus grâce au modèle choisit et nous les commenterons. Nous conclurons enfin en caractérisant ce qui influence le plus les ménages quant à leur choix de mode de transport pour partir en vacance.
Tout d’abord, nous allons effectuer quelques statistiques descriptives afin de nous approprier les données et avoir une vision globale de l’échantillon sur lequel nous allons travailler. 
