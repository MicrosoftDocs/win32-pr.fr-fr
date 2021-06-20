---
description: En savoir plus sur la prise en charge des fonctions mathématiques dans D3DX. D3DX est une bibliothèque d’utilitaire qui fournit des services d’assistance. Il s’agit d’une couche au-dessus du composant Direct3D.
ms.assetid: a44d25de-f79d-4132-a75a-0c22ccd84341
title: Prise en charge des fonctions mathématiques dans D3DX (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a28c32b13d185694e4ffa41c314cf9f77cbb18b7
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112407522"
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

 

 



