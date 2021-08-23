---
description: En savoir plus sur la prise en charge des fonctions mathématiques dans D3DX. D3DX est une bibliothèque d’utilitaire qui fournit des services d’assistance. Il s’agit d’une couche au-dessus du composant Direct3D.
ms.assetid: a44d25de-f79d-4132-a75a-0c22ccd84341
title: Prise en charge des fonctions mathématiques dans D3DX (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c77e3d75c692d4801e6a8af64bd980e72eb88f0d3276ff4e1364302b5a62357d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119368969"
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

 

 



