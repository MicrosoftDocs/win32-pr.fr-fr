---
description: D3DX est une bibliothèque d’utilitaire qui fournit des services d’assistance. Il s’agit d’une couche au-dessus du composant Direct3D.
ms.assetid: a44d25de-f79d-4132-a75a-0c22ccd84341
title: Prise en charge des fonctions mathématiques dans D3DX (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac69e0385919b015d1f8d3e7d47e221c06a04fbb
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109151"
---
# <a name="math-function-support-in-d3dx-direct3d-9"></a>Prise en charge des fonctions mathématiques dans D3DX (Direct3D 9)

D3DX est une bibliothèque d’utilitaire qui fournit des services d’assistance. Il s’agit d’une couche au-dessus du composant Direct3D.

## <a name="math"></a>Math

La prise en charge des mathématiques, contenue dans un ensemble de fonctions, est fournie pour :

-   Calculs de couleur
-   Appareils
-   Manipulation de matrice
-   Quaternions
-   vecteurs 2D
-   vecteurs 3D
-   vecteurs 4D

Notez qu’en cas d’association avec les surcharges C++, la prise en charge des types mathématiques de base en 3D est complète.

Pour plus d’informations sur ces fonctions, consultez [D3DX Functions](dx9-graphics-reference-d3dx-functions.md). Pour vous aider à trouver la fonction dont vous avez besoin, elles sont réparties dans plusieurs dossiers.

## <a name="float16"></a>FLOAT16

Lorsque vous utilisez le type de données FLOAT16, veillez à limiter les valeurs à un maximum de D3DX \_ 16F \_ Max. Toute valeur FLOAT16 dépassant cela entraînera un comportement indéfini dans le pipeline. Consultez [les autres constantes D3DX](other-d3dx-constants.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[D3DX](d3dx.md)
</dt> </dl>

 

 



