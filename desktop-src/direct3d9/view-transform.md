---
description: Cette section présente les concepts de base de la transformation de vue et fournit des détails sur la configuration d’une matrice de transformation de vue dans une application Direct3D.
ms.assetid: a9885a77-f04e-4ca5-9202-67c4779d03de
title: Vue de la transformation (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60cf933db7424b2c3aeb5aa7c06a37b03782eaa6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521908"
---
# <a name="view-transform-direct3d-9"></a>Vue de la transformation (Direct3D 9)

Cette section présente les concepts de base de la transformation de vue et fournit des détails sur la configuration d’une matrice de transformation de vue dans une application Direct3D.

La transformation de vue localise la visionneuse dans l’espace universel, en transformant les vertex en espace de caméra. Dans l’espace de l’appareil photo, l’appareil photo, ou la visionneuse, est à l’origine, en regardant l’axe z positif. Rappelez-vous que Direct3D utilise un système de coordonnées gauche, donc z est positif dans une scène. La matrice de vue déplace les objets dans le monde autour de la position d’un appareil photo : l’origine de l’espace et de l’orientation de l’appareil photo.

Il existe plusieurs façons de créer une matrice de vue. Dans tous les cas, la caméra a une position logique et une orientation dans l’espace universel qui est utilisée comme point de départ pour créer une matrice de vue qui sera appliquée aux modèles dans une scène. La matrice de vue traduit et fait pivoter les objets pour les placer dans l’espace de l’appareil photo, où l’appareil photo est à l’origine. Une façon de créer une matrice de vue consiste à combiner une matrice de translation avec des matrices de rotation pour chaque axe. Dans cette approche, l’équation de matrice générale suivante s’applique.

![équation de la transformation de la vue](images/viewtran.png)

Dans cette formule, V est la matrice de vue en cours de création, T est une matrice de translation qui repositionne les objets dans le monde, et R ₓ à R<sub>z</sub> sont des matrices de rotation qui font pivoter les objets le long des axes x, y et z. Les matrices translation et rotation sont basées sur la position logique et l’orientation de l’appareil photo dans l’espace universel. Donc, si la position logique de l’appareil photo dans le monde est <10 20100>, l’objectif de la matrice de translation est de déplacer les objets de 10 unités le long de l’axe x,-20 unités le long de l’axe y et-100 unités le long de l’axe z. Les matrices de rotation de la formule sont basées sur l’orientation de l’appareil photo, en termes d’alignement de l’espace de l’appareil photo par rapport à l’espace universel. Par exemple, si l’appareil photo mentionné précédemment pointe vers le haut, son axe z est de 90 degrés (pi/2 radians) hors alignement avec l’axe z de l’espace universel, comme indiqué dans l’illustration suivante.

![illustration de l’espace d’affichage de la caméra par rapport à l’espace universel](images/camtop.png)

Les matrices de rotation appliquent des rotations de grandeur égale, mais opposée, aux modèles de la scène. La matrice de vue pour cette caméra comprend une rotation de-90 degrés autour de l’axe x. La matrice de rotation est associée à la matrice de translation pour créer une matrice de vue qui ajuste la position et l’orientation des objets dans la scène afin que le haut de la caméra soit orienté vers la caméra, ce qui donne l’impression que l’appareil photo est au-dessus du modèle.

## <a name="setting-up-a-view-matrix"></a>Configuration d’une matrice de vue

Les fonctions d’assistance [**D3DXMatrixLookAtLH**](d3dxmatrixlookatlh.md) et [**D3DXMatrixLookAtRH**](d3dxmatrixlookatrh.md) créent une matrice de vue basée sur l’emplacement de l’appareil photo et un point d’affichage.

L’exemple suivant crée une matrice de vue pour les coordonnées de gauche.


```
D3DXMATRIX out;
D3DXVECTOR3 eye(2,3,3);
D3DXVECTOR3 at(0,0,0);
D3DXVECTOR3 up(0,1,0);
D3DXMatrixLookAtLH(&out, &eye, &at, &up);
```



Direct3D utilise les matrices universelles et de vue pour configurer plusieurs structures de données internes. Chaque fois que vous définissez une nouvelle matrice de monde ou d’affichage, le système recalcule les structures internes associées. La définition fréquente de ces matrices est fastidieuse. Vous pouvez réduire le nombre de calculs requis en concaténant votre monde et en vue des matrices dans une matrice de vue universelle que vous définissez comme matrice universelle, puis en définissant la matrice de vue sur l’identité. Conservez les copies mises en cache des matrices de monde et de vue individuelles que vous pouvez modifier, concaténer et réinitialiser la matrice universelle en fonction des besoins. Par souci de clarté, les exemples utilisent rarement cette optimisation.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Transformations](transforms.md)
</dt> </dl>

 

 



