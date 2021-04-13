---
description: La fusion de vertex indexée étend la prise en charge de la fusion de vertex dans Direct3D pour permettre l’utilisation de matrices pour la fusion.
ms.assetid: d320cb8a-48b6-4a53-a051-d50f239c1aa3
title: Fusion de vertex indexée (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4cfe7b45831317fdf9e92525ed74bbd27323e99
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104480713"
---
# <a name="indexed-vertex-blending-direct3d-9"></a>Fusion de vertex indexée (Direct3D 9)

La fusion de vertex indexée étend la prise en charge de la fusion de vertex dans Direct3D pour permettre l’utilisation de matrices pour la fusion. Ces matrices sont référencées à l’aide d’un index de matrice. Ces index sont fournis sur la base de chaque vertex et font référence à une palette allant jusqu’à 256 matrices. Chaque index est constitué de 8 bits et chaque vertex peut avoir jusqu’à quatre index, ce qui permet de mélanger quatre matrices par vertex. Les index sont empaquetés dans un DWORD. Étant donné que les index sont spécifiés sur une base par vertex, jusqu’à 12 matrices peuvent affecter un seul triangle, et toute matrice de la palette peut affecter les vertex d’un appel de dessin. Cette approche présente les avantages suivants :

-   Il permet à plus de matrices d’affecter un seul triangle.
-   Il permet à d’autres triangles mélangés d’être passés dans le même appel de dessin.
-   Il rend la fusion de vertex indépendante des indices de triangle. Cela permet aux maillages progressifs de fonctionner conjointement avec la fusion de vertex.

L’un des inconvénients de cette approche est qu’elle ne fonctionne pas avec les primitives de surface courbée quand le pavage se produit avant le traitement du vertex.

Le diagramme suivant montre comment quatre matrices peuvent affecter un vertex. Chaque vertex compte jusqu’à quatre index, quatre matrices peuvent donc être mélangées par vertex. Le diagramme utilise les matrices indexées à 0, 2, 5 et 6.

![diagramme de la fusion des vertex indexés à l’aide de 4 matrices disponibles de 256](images/dword1.png)

Le diagramme suivant montre comment 12 matrices au maximum peuvent affecter un triangle. L’utilisation des index spécifiés sur une base par vertex, jusqu’à 12 matrices peut affecter le triangle.

![diagramme de la fusion des vertex indexés pour un triangle à l’aide de 12 matrices disponibles de 12 256](images/dword2.png)

L’équation suivante détermine le cas général de l’effet des matrices sur un sommet.

![équation de la fusion des vertex indexés](images/indexedvblend.png)

Le <sub>modèle</sub> V est la position du vertex de l’espace du modèle d’entrée. Index0.. Index3 sont les index de matrice par vertex compressés dans une valeur DWORD. M \[ \] est le tableau de matrices universelles qui sont indexées dans. b ₀.. b ₂ sont les pondérations de fusion. Le<sub>monde</sub> V est la position du sommet de l’espace universel de sortie.

Pour plus d’informations sur la fusion des vertex indexés, consultez Utilisation de la [fusion de vertex indexée (Direct3D 9)](using-indexed-vertex-blending.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Fusion géométrique](geometry-blending.md)
</dt> </dl>

 

 



