---
title: Effet de redresser
description: Pivote et ajuste éventuellement une image.
ms.assetid: aa37cdf1-bbb6-db4e-45a7-67c7cc16b7b4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a8e521ca4c0c452301c0f8031c94ba8c22efe80
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127112518"
---
# <a name="straighten-effect"></a>Effet de redresser

Pivote et ajuste éventuellement une image.

Le CLSID de cet effet est CLSID \_ D2D1Straighten.

-   [Exemple d’image](#example-image)
-   [Exemple de Code](#sample-code)
-   [Propriétés d’effet](#effect-properties)
-   [Configuration requise](#requirements)
-   [Rubriques connexes](#related-topics)

## <a name="example-image"></a>Exemple d’image

![exemple de sortie d’effet](images/straighten-effect.png)

## <a name="sample-code"></a>Exemple de code


```cpp
ComPtr<ID2D1Effect> straightenEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Straighten, &straightenEffect);
 
straightenEffect->SetInput(0, bitmap);
straightenEffect->SetValue(D2D1_STRAIGHTEN_PROP_ANGLE, 12.0f);
straightenEffect->SetValue(D2D1_STRAIGHTEN_PROP_MAINTAIN_SIZE, true);
straightenEffect->SetValue(D2D1_STRAIGHTEN_PROP_SCALE_MODE, D2D1_STRAIGHTEN_SCALE_MODE_LINEAR);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(straightenEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a>Propriétés d’effet

Les propriétés de l’effet redresser sont définies par l’énumération [**d2d1 \_ redresse \_ prop**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_straighten_prop) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------------|---------------------------------------------------|
| Client minimal pris en charge | Windows 10 \[ applications de bureau \| Windows applications du windows Store\] |
| Serveur minimal pris en charge | Windows 10 \[ applications de bureau \| Windows applications du windows Store\] |
| En-tête                   | d2d1effects \_ 2. h                                  |
| Bibliothèque                  | d2d1. lib, dxguid. lib                              |


## <a name="related-topics"></a>Rubriques connexes

* [Interface ID2D1Effect](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)

