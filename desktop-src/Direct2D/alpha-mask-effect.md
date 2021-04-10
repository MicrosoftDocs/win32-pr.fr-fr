---
title: Effet masque Alpha
description: Cet effet applique un masque Alpha à une image. Il a deux entrées, nommées destination et Mask. Les valeurs de couleur de l’image de destination sont multipliées par le canal alpha de l’image de masque.
ms.assetid: fddad107-ec70-3a24-f4ae-9dc4f3716536
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87669608ab75ab7a655c072e174dbcd19df4bb39
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106561"
---
# <a name="alpha-mask-effect"></a>Effet masque Alpha

Cet effet applique un masque Alpha à une image. Il a deux entrées, nommées destination et Mask. Les valeurs de couleur de l’image de destination sont multipliées par le canal alpha de l’image de masque.

Le CLSID de cet effet est CLSID \_ D2D1AlphaMask.

## <a name="effect-properties"></a>Propriétés d’effet

Cet effet n’a aucune propriété propre à l’effet.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------------|---------------------------------------------------|
| Client minimal pris en charge | Applications de \[ Bureau Windows 10 \| applications du Windows Store\] |
| Serveur minimal pris en charge | Applications de \[ Bureau Windows 10 \| applications du Windows Store\] |
| En-tête                   | d2d1effects \_ 2. h                                  |
| Bibliothèque                  | d2d1. lib, dxguid. lib                              |

## <a name="related-topics"></a>Rubriques connexes

* [Interface ID2D1Effect](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)

