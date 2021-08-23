---
title: Registres-hs_5_0
description: 'Un nuanceur de coque se compose de trois phases : phase de point de contrôle, phase de branchement et phase de jointure distinctes. Chaque phase a ses propres jeux de registres d’entrée et de sortie.'
ms.assetid: 82F689EF-D3F4-40B5-9A2C-1F97F4CE6501
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3891130b4a952cb991615dbcc386e245d5eb8abedc2d8cec0b441eb6b3c2fbae
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119854029"
---
# <a name="registers---hs_5_0"></a>Registres-HS \_ 5 \_ 0

Un nuanceur de coque se compose de trois phases distinctes : la phase de point de contrôle, la phase de branchement et la phase de jointure. Chaque phase a ses propres jeux de registres d’entrée et de sortie.

## <a name="control-point-phase"></a>Phase de point de contrôle

\_ \_ la phase du point de contrôle HS \_ est un programme de nuanceur avec le modèle d’inscription suivant.

### <a name="input-registers"></a>Registres d’entrée



| Type de Registre                                     | Count                 | R/W (Lecture/écriture) | Dimension | Indexable par r\# | Valeurs par défaut | DCL obligatoire |
|---------------------------------------------------|-----------------------|-----|-----------|------------------|----------|--------------|
| Temp 32 bits (r \# )                                 | 4096 (r \# + x \# \[ n \] )    | R/W (Lecture/écriture) | 4         | Non               | None     | Oui          |
| Tableau Temp indexable 32 bits (x \# \[ n \] )            | 4096 (r \# + x \# \[ n \] )    | R/W (Lecture/écriture) | 4         | Oui              | None     | Oui          |
| Entrée 32 bits ( \[ élément sommet v \] \[ \] )             | 32 (élément) \* 32 (vert) | R   | 4         | Oui              | None     | Oui          |
| vOutputControlPointID d’entrée UINT de 32 bits (23.7)     | 1                     | R   | 1         | Non               | None     | Oui          |
| PrimitiveID d’entrée UINT de 32 bits (vPrim)             | 1                     | R   | 1         | Non               | N/A      | Oui          |
| Élément dans une ressource d’entrée (t \# )                | 128                   | R   | 128       | Oui              | None     | Oui          |
| Échantillonneur (s \# )                                     | 16                    | R   | 1         | Oui              | None     | Oui          |
| Référence ConstantBuffer ( \# \[ index CB \] )          | 15                    | R   | 4         | Oui              | None     | Oui          |
| Référence ConstantBuffer immédiate ( \[ index ICB \] ) | 1                     | R   | 4         | Oui (contenu)   | Aucun     | Oui          |



 

### <a name="output-registers"></a>Registres de sortie



| Type de Registre                           | Count | R/W (Lecture/écriture) | Dimension | Indexable par r\# | Valeurs par défaut | DCL obligatoire |
|-----------------------------------------|-------|-----|-----------|------------------|----------|--------------|
| Élément de données de vertex de sortie 32 bits (o \# ) | 32    | W   | 4         | Oui              | None     | Oui          |



 

Chaque registre de sortie de la phase du point de contrôle de nuanceur de coque est jusqu’à un vecteur à 4, dont jusqu’à 32 registres peuvent être déclarés. Il y a également entre 1 et 32 points de contrôle de sortie déclarés, ce qui met à l’échelle la quantité de stockage requise. Reportez-vous au nombre maximal d’agrégats autorisés pour la sortie de la phase du point de contrôle de nuanceur de coque en tant que \# \_ sortie CP \_ Max.

\#\_ \_ Nbre max. de sortie cp = 3968 scalaires.

Cette limite est basée sur un point de conception pour un certain matériel de 4096 de \* stockage 32 bits ici. La valeur de la sortie du point de contrôle est de 3968 = 4096-128, qui est 32 (points de contrôle) \* 4 (composants) \* 32 (éléments)-4 (composants) \* 32 (éléments). La soustraction réserve 128 scalaires (un point de contrôle) de l’espace réservé au nuanceur de coque phase 2 et 3. Le choix de la réservation de 128 scalaires pour les constantes de correctifs, plutôt que d’autoriser tout simplement l’un des 4096 scalaires de stockage n’est pas utilisé par les points de contrôle de sortie, en prenant en compte les limites d’une conception matérielle particulière. La phase du point de contrôle peut déclarer des points de contrôle de sortie 32, mais elle ne peut pas être entièrement 32 d’éléments avec 4 composants chacun, car le stockage total est trop élevé.

## <a name="fork-phase"></a>Phase de fourche

Les registres suivants sont visibles dans le modèle de \_ phase de bifurcation SH \_ .

Les ressources d’entrée (t \# ), les échantillonneurs \# , les mémoires tampons constantes (CB \# ) et le tampon de constante immédiate (ICB) ci-dessous sont tous des États partagés avec toutes les autres phases de nuanceur de coque. Autrement dit, du point de vue de l’API/DDI, le nuanceur de coque possède un ensemble unique d’États des ressources d’entrée pour toutes les phases. Cela va du fait que du point de vue API/DDI, le nuanceur de coque est un nuanceur atomique unique. les phases qu’il contient sont des détails d’implémentation.

### <a name="input-registers"></a>Registres d’entrée



| Type de Registre                                                                         | Count              | R/W (Lecture/écriture) | Dimension                           | Indexable par r\# | Valeurs par défaut | DCL obligatoire |
|---------------------------------------------------------------------------------------|--------------------|-----|-------------------------------------|------------------|----------|--------------|
| Temp 32 bits (r \# )                                                                     | 4096 (r \# + x \# \[ n \] ) | R/W (Lecture/écriture) | 4                                   | Non               | None     | Oui          |
| Tableau Temp indexable 32 bits (x \# \[ n \] )                                                | 4096 (r \# + x \# \[ n \] ) | R/W (Lecture/écriture) | 4                                   | Oui              | None     | Oui          |
| Points de contrôle d’entrée 32 bits ( \[ élément VICP vertex \] \[ \] ) (phase de précontrôle du point)     | 32 Voir la remarque ci-dessous  | R   | 4 (composant) \* 32 (élément) \* 32 (vert) | Oui              | None     | Oui          |
| Points de contrôle de sortie 32 bits ( \[ élément vocp vertex \] \[ \] \] ) (phase de point de contrôle) | 32 Voir la remarque ci-dessous  | R   | 4 (composant) \* 32 (élément) \* 32 (vert) | Oui              | None     | Oui          |
| PrimitiveID d’entrée UINT de 32 bits (vPrim)                                                 | 1                  | R   | 1                                   | Non               | N/A      | Oui          |
| ForkInstanceID d’entrée UINT de 32 bits (23.8) (vForkInstanceID)                              | 1                  | R   | 1                                   | Non               | N/A      | Oui          |
| Élément dans une ressource d’entrée (t \# )                                                    | 128                | R   | 128                                 | Oui              | None     | Oui          |
| Échantillonneur (s \# )                                                                         | 16                 | R   | 1                                   | Oui              | None     | Oui          |
| Référence ConstantBuffer ( \# \[ index CB \] )                                              | 15                 | R   | 4                                   | Oui              | None     | Oui          |
| Référence ConstantBuffer immédiate ( \[ index ICB \] )                                     | 1                  | R   | 4                                   | Oui (contenu)   | Aucun     | Oui          |



 

> [!Note]
> Les déclarations de point de contrôle d’entrée (VICP) de la phase de bifurcation du nuanceur de coque doivent correspondre à n’importe quel sous-ensemble, le long \[ \] de l’axe des éléments, de l’entrée du point de contrôle de nuanceur de coque (phase de précontrôle du point de contrôle) De même, les déclarations permettant de saisir les points de contrôle de sortie (vocp) doivent être n’importe quel sous-ensemble, le long \[ \] de l’axe des éléments, des points de contrôle de sortie de nuanceur de coque (phase de point de contrôle).
> 
> Le long de l' \[ axe du vertex \] , le nombre de points de contrôle à lire pour chaque VICP et vocp doit être similaire à un sous-ensemble du nombre de points de contrôle d’entrée du nuanceur de coque et du nombre de points de contrôle de sortie du nuanceur de coque, respectivement. Par exemple, si l’axe des vertex des registres vocp est déclaré avec n vertex, qui rend les points de contrôle de sortie de la phase du point de contrôle \[ 0.. n-1 \] disponibles en tant qu’entrée en lecture seule à la phase de fourche.

### <a name="output-registers"></a>Registres de sortie



| S’inscrire                                        | Count               | R/W (Lecture/écriture) | Dimension | Indexable par r\# | Valeurs par défaut | DCL obligatoire |
|-------------------------------------------------|---------------------|-----|-----------|------------------|----------|--------------|
| Élément de données de constante de correctif de sortie 32 bits (o \# ) | 32 Voir la remarque 1 ci-dessous | W   | 4         | Oui              | None     | Oui          |



 

> [!Note]  
> Les sorties de la phase de jointure et de bifurcation du nuanceur de coque sont un ensemble partagé de registres 4 4-Vector. Les sorties de chaque programme de la phase de jointure ou de branche ne peuvent pas se chevaucher. Les valeurs interprétées par le système, telles que TessFactors, proviennent de cet espace.

## <a name="join-phase"></a>Phase de jointure

Les registres suivants sont visibles dans le modèle de \_ phase de jointure HS \_ . Il existe trois ensembles de registres d’entrée : les points de contrôle d’entrée de phase de contrôle (VICP), les points de contrôle de sortie de phase de contrôle vocp (vocp) et les constantes correctives (VCP). VPC est la sortie agrégée de tous les programmes de la phase de bifurcation du nuanceur de coque. Les registres de sortie de la phase de jointure du nuanceur \# de coque se trouvent dans le même espace de registre que les sorties de la phase de bifurcation du nuanceur de coque.

Les ressources d’entrée (t \# ), les échantillonneurs \# , les mémoires tampons constantes (CB \# ) et le tampon de constante immédiate (ICB) ci-dessous sont tous des États partagés avec toutes les autres phases de nuanceur de coque. Autrement dit, du point de vue de l’API/DDI, le nuanceur de coque possède un ensemble unique d’États des ressources d’entrée pour toutes les phases. Cela va du fait que du point de vue API/DDI, le nuanceur de coque est un nuanceur atomique unique. les phases qu’il contient sont des détails d’implémentation.

### <a name="input-registers"></a>Registres d’entrée



| Type de Registre                                                                       | Count               | R/W (Lecture/écriture) | Dimension                           | Indexable par r\# | Valeurs par défaut | DCL obligatoire |
|-------------------------------------------------------------------------------------|---------------------|-----|-------------------------------------|------------------|----------|--------------|
| Temp 32 bits (r \# )                                                                   | 4096 (r \# + x \# \[ n \] )  | R/W (Lecture/écriture) | 4                                   | Non               | None     | Oui          |
| Tableau Temp indexable 32 bits (x \# \[ n \] )                                              | 4096 (r \# + x \# \[ n \] )  | R/W (Lecture/écriture) | 4                                   | Oui              | None     | Oui          |
| Points de contrôle d’entrée 32 bits ( \[ élément VICP vertex \] \[ \] ) (phase de précontrôle du point)   | 32 Voir la remarque 1 ci-dessous | R   | 4 (composant) \* 32 (élément) \* 32 (vert) | Oui              | None     | Oui          |
| Points de contrôle de sortie 32 bits ( \[ élément vocp vertex \] \[ \] ) (phase de point de contrôle) | 32 Voir la remarque 1 ci-dessous | R   | 4 (composant) \* 32 (élément) \* 32 (vert) | Oui              | None     | Oui          |
| Entrée 32 bits (élément VPC \[ \] ) (données de constante de correctif)                                 | 32 Voir la remarque 2 ci-dessous | R   | 4                                   | Oui              | None     | Oui          |
| PrimitiveID d’entrée UINT de 32 bits (vPrim)                                               | 1                   | R   | 1                                   | Non               | N/A      | Oui          |
| JoinInstanceID d’entrée UINT de 32 bits (vJoinInstanceID)                                  | 1                   | R   | 1                                   | Non               | N/A      | Oui          |
| Élément dans une ressource d’entrée (t \# )                                                  | 128                 | R   | 128                                 | Oui              | None     | Oui          |
| Échantillonneur (s \# )                                                                       | 16                  | R   | 1                                   | Oui              | None     | Oui          |
| Référence ConstantBuffer ( \# \[ index CB \] )                                            | 15                  | R   | 4                                   | Oui              | None     | Oui          |
| Référence ConstantBuffer immédiate ( \[ index ICB \] )                                   | 1                   | R   | 4                                   | Oui (contenu)   | Aucun     | Oui          |



 

**Remarque 1 :** Les déclarations de point de contrôle d’entrée (VICP) de la phase de jointure du nuanceur de coque doivent correspondre à n’importe quel sous-ensemble, le long \[ \] de l’axe des éléments, de l’entrée du point de contrôle de nuanceur de coque (phase de précontrôle du point de contrôle) De même, les déclarations permettant de saisir les points de contrôle de sortie (vocp) doivent être n’importe quel sous-ensemble, le long \[ \] de l’axe des éléments, des points de contrôle de sortie de nuanceur de coque (phase de point de contrôle).

Le long de l' \[ axe du vertex \] , le nombre de points de contrôle à lire pour chaque VICP et vocp doit être similaire à un sous-ensemble du nombre de points de contrôle d’entrée du nuanceur de coque et du nombre de points de contrôle de sortie du nuanceur de coque, respectivement. Par exemple, si l’axe des vertex des registres vocp est déclaré avec n vertex, qui rend les points de contrôle de sortie de la phase du point de contrôle \[ 0.. n-1 \] disponibles en tant qu’entrée en lecture seule à la phase de jointure.

**Remarque 2 :** En plus de l’entrée de point de contrôle, la phase de jointure du nuanceur de coque voit également comme entrée les données de constante de patch calculées par le ou les programmes de la phase de bifurcation du nuanceur de coque. Cela s’affiche lors de la phase de bifurcation du nuanceur de coque lorsque l’enregistrement VPC est \# inscrit. Les registres VPC d’entrée de la phase de jointure du nuanceur de coque \# partagent le même espace d’enregistrement que les registres o de la phase de fourche du nuanceur de coque \# . Les déclarations des registres o \# ne doivent pas se chevaucher avec une déclaration de sortie du programme de la phase fourche du nuanceur de coque \# . la phase de jointure du nuanceur de coque est ajoutée à la sortie de données de constante de patch de l’agrégat pour le nuanceur de coque.

### <a name="output-registers"></a>Registres de sortie



| Type de Registre                                   | Count             | R/W (Lecture/écriture) | Dimension | Indexable par r\# | Valeurs par défaut | DCL obligatoire |
|-------------------------------------------------|-------------------|-----|-----------|------------------|----------|--------------|
| Élément de données de constante de correctif de sortie 32 bits (o \# ) | 32 Voir la remarque ci-dessous | W   | 4         | Oui              | None     | Oui          |



 

> [!Note]  
> Les sorties de la phase de jointure et de bifurcation du nuanceur de coque sont un ensemble partagé de registres 4 4-Vector. Les sorties de chaque programme de la phase de jointure ou de branche ne peuvent pas se chevaucher. Les valeurs interprétées par le système, telles que TessFactors, proviennent de cet espace.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Shader, modèle 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




