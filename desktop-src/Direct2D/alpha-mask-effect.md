---
title: Effet masque Alpha
description: Cet effet applique un masque Alpha à une image. Il a deux entrées, nommées destination et Mask. Les valeurs de couleur de l’image de destination sont multipliées par le canal alpha de l’image de masque.
ms.assetid: fddad107-ec70-3a24-f4ae-9dc4f3716536
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed4c9c205f7f19c3fa43d95ee92a70d7d43ed709b40c924165833fab7190e3b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119570549"
---
# <a name="alpha-mask-effect"></a>Effet masque Alpha

Cet effet applique un masque Alpha à une image. Il a deux entrées, nommées destination et Mask. Les valeurs de couleur de l’image de destination sont multipliées par le canal alpha de l’image de masque.

Le CLSID de cet effet est CLSID \_ D2D1AlphaMask.

## <a name="effect-properties"></a>Propriétés d’effet

Cet effet n’a aucune propriété propre à l’effet.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------------|---------------------------------------------------|
| Client minimal pris en charge | Windows 10 \[ applications de bureau \| Windows applications du windows Store\] |
| Serveur minimal pris en charge | Windows 10 \[ applications de bureau \| Windows applications du windows Store\] |
| En-tête                   | d2d1effects \_ 2. h                                  |
| Bibliothèque                  | d2d1. lib, dxguid. lib                              |

## <a name="related-topics"></a>Rubriques connexes

* [Interface ID2D1Effect](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)

