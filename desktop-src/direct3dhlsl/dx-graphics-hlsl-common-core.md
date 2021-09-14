---
title: Common-Shader Core
description: Common-Shader Core
ms.assetid: f3cf2969-83a4-461f-8177-d336536194ba
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 66c1f763c4771a8406acd2f3401445d1a29cde79
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126854949"
---
# <a name="common-shader-core"></a>Common-Shader Core

Dans le nuanceur modèle 4, toutes les étapes de nuanceur implémentent les mêmes fonctionnalités de base à l’aide d’un noyau de nuanceur commun. En outre, chacune des trois étapes de nuanceur (vertex, Geometry et pixel) offre des fonctionnalités uniques à chaque étape, telles que la possibilité de générer de nouvelles primitives à partir de l’étape de nuanceur Geometry ou d’ignorer un pixel spécifique dans l’étape de nuanceur de pixels. Le diagramme suivant illustre la façon dont les données circulent dans une étape de nuanceur, ainsi que la relation entre le noyau-nuanceur commun et les ressources de mémoire du nuanceur.

![diagramme du workflow de données dans une étape de nuanceur](images/d3d10-shader-unit.png)

-   **Données d’entrée**: un nuanceur de sommets reçoit ses entrées de l’étape assembleur d’entrée ; les nuanceurs de géométrie et de pixels reçoivent leurs entrées de l’étape de nuanceur précédente. Les entrées supplémentaires incluent la [sémantique de valeur système](dx-graphics-hlsl-semantics.md), qui sont consommables par la première unité dans le pipeline auquel elles s’appliquent.
-   **Données de sortie**: les nuanceurs génèrent des résultats de sortie à passer à l’étape suivante dans le pipeline. Pour un nuanceur Geometry, la quantité de données générées par un appel unique peut varier. Certaines sorties sont interprétées par le Common-Shader Core (par exemple, position de vertex et index de tableau de cibles de rendu), d’autres sont conçues pour être interprétées par une application.
-   **Code du nuanceur**: les nuanceurs peuvent lire à partir de la mémoire, effectuer des opérations arithmétiques de vecteurs et d’entiers, ou effectuer des opérations de contrôle de Workflow. Il n’existe aucune limite quant au nombre d’instructions qui peuvent être implémentées dans un nuanceur.
-   **Échantillonneurs**: les échantillonneurs définissent comment échantillonner et filtrer les textures. Jusqu’à 16 échantillons peuvent être liés simultanément à un nuanceur.
-   **Textures**: les textures peuvent être filtrées à l’aide d’échantillonneurs ou lues sur une base par Texel directement avec la fonction intrinsèque [Load](dx-graphics-hlsl-to-load.md) .
-   **Mémoires tampons**: les mémoires tampons ne sont jamais filtrées, mais peuvent être lues à partir de la mémoire à chaque élément directement avec la fonction intrinsèque [Load](dx-graphics-hlsl-to-load.md) . Jusqu’à 128 de ressources de texture et de mémoire tampon (combinées) peuvent être liées simultanément à un nuanceur.
-   **Mémoires tampons constantes**: les mémoires tampons constantes sont optimisées pour les variables constantes de nuanceur. Jusqu’à 16 mémoires tampons constantes peuvent être liées simultanément à une étape de nuanceur. Elles sont conçues pour des mises à jour plus fréquentes à partir de l’UC. par conséquent, elles ont des restrictions de taille, de mise en page et d’accès supplémentaires.


Différences entre Direct3D 9 et Direct3D 10 :

- Dans Direct3D 9, chaque unité de nuanceur avait un seul fichier de registre de constantes de petite taille pour stocker toutes les variables de nuanceur constantes. L’utilisation de tous les nuanceurs avec cet espace constant limité nécessitait un recyclage fréquent des constantes par le processeur.
- Dans Direct3D 10, les constantes sont stockées dans des mémoires tampons immuables en mémoire et sont gérées comme n’importe quelle autre ressource. Il n’existe pas de limite au nombre de mémoires tampons constantes qu’une application peut créer. En organisant des constantes dans des mémoires tampons en fonction de la fréquence des mises à jour et de l’utilisation, la quantité de bande passante requise pour mettre à jour les constantes pour prendre en charge tous les nuanceurs peut être considérablement réduite.



 

## <a name="integer-and-bitwise-support"></a>Prise en charge des bits et des entiers

Le Common Shader Core fournit un ensemble complet d’opérations au niveau du bit et d’entier 32 bits conformes à IEEE. Ces opérations activent une nouvelle classe d’algorithmes dans des exemples de matériel graphique, notamment des techniques de compression et d’empaquetage, FFTs et un contrôle de déroulement de programme de champ de bits.

Les types de données **int** et **uint** dans Direct3D 10 HLSL sont mappés à des entiers 32 bits dans le matériel.



|                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Différences entre Direct3D 9 et Direct3D 10 :<br/> Dans Direct3D 9, les entrées marquées comme étant des entiers en HLSL étaient interprétées comme étant à virgule flottante. Dans Direct3D 10, les entrées de flux marquées comme Integer sont interprétées comme un entier 32 bits.<br/> En outre, les valeurs booléennes sont maintenant tous les bits définis ou tous les bits non définis. Les données converties en **bool** seront interprétées comme true si la valeur n’est pas égale à 0.0 f (les valeurs NULL positives et négatives sont autorisées à être false) et false dans le cas contraire.<br/> |



 

## <a name="bitwise-operators"></a>Opérateurs au niveau du bit

Le Common Shader Core prend en charge les opérateurs de bits suivants :



| Opérateur  | Fonction          |
|-----------|-------------------|
| ~         | NOT logique       |
| <<  | Décalage vers la gauche        |
| >>  | Décalage vers la droite       |
| &         | AND logique       |
| \|        | Or logique        |
| ^         | XOR logique       |
| <<= | Décalage vers la gauche égal  |
| >>= | Décalage vers la droite égal |
| &=        | Et égal à         |
| \|=       | Ou égal à          |
| ^=        | XOR égal         |



 

Les opérateurs au niveau du bit sont définis pour fonctionner uniquement sur les types de données **int** et **uint** . Toute tentative d’utilisation d’opérateurs de bits sur des types de données **float** ou **struct** génère une erreur. Les opérateurs au niveau du bit suivent la même priorité que C en ce qui concerne les autres opérateurs.

## <a name="binary-casts"></a>Casts binaires

Le cast entre un entier et un type à virgule flottante convertit la valeur numérique à la suite des règles de troncation C. Effectuer un cast d’une valeur d’un **float** vers un **int**, puis revenir à un **float** est une conversion avec perte dépendante de la précision du type de données cible. Voici quelques-unes des fonctions de conversion : [**asfloat (DirectX HLSL)**](dx-graphics-hlsl-asfloat.md), [**ASINT (DirectX HLSL)**](dx-graphics-hlsl-asint.md), [**asuint (DirectX HLSL)**](dx-graphics-hlsl-asuint.md).

Les casts binaires peuvent également être effectués à l’aide de fonctions intrinsèques HLSL. En conséquence, le compilateur réinterprète la représentation sous forme de bit d’un nombre dans le type de données cible.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Nuanceur modèle 4](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 





