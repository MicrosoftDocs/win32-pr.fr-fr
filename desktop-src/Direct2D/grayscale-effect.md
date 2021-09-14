---
title: Effet de nuances de gris
description: convertit une image en gris monochrome.
ms.assetid: 4e0b26ed-ba71-5f8f-db1e-f1b4e28fbd11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0dc3cb6a807d282649a2826713cdf48fa966d9f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127113197"
---
# <a name="grayscale-effect"></a>Effet de nuances de gris

convertit une image en gris monochrome.

Le gris utilise l’effet de matrice de couleurs pour convertir en nuances de gris, à l’aide de la matrice suivante :

![matrice de conversion](images/grayscale-effect-matrix.png)

Le CLSID de cet effet est CLSID \_ D2D1Grayscale.

-   [Exemple d’image](#example-image)
-   [Propriétés d’effet](#effect-properties)
-   [Configuration requise](#requirements)
-   [Rubriques connexes](#related-topics)

## <a name="example-image"></a>Exemple d’image

![exemple de sortie d’effet](images/grayscale-effect.png)

## <a name="effect-properties"></a>Propriétés d’effet

Cet effet n’a pas de propriétés.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------------|---------------------------------------------------|
| Client minimal pris en charge | Windows 10 \[ applications de bureau \| Windows applications du windows Store\] |
| Serveur minimal pris en charge | Windows 10 \[ applications de bureau \| Windows applications du windows Store\] |
| En-tête                   | d2d1effects \_ 2. h                                  |
| Bibliothèque                  | d2d1. lib, dxguid. lib                              |


## <a name="related-topics"></a>Rubriques connexes

* [Interface ID2D1Effect](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
