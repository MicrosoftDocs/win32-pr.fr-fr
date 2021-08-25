---
title: Effet Postérisation
description: L’effet Postérisation réduit le nombre de couleurs uniques dans une image.
ms.assetid: e6686998-1246-b3b7-6f4f-212568c3191c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21372ee43935441168609cc81ef053ac96fd3fdbbd7cd3c16578f13d1a47fda1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119636102"
---
# <a name="posterize-effect"></a>Effet Postérisation

L’effet Postérisation réduit le nombre de couleurs uniques dans une image.

Le CLSID de cet effet est CLSID \_ D2D1Posterize.

-   [Exemple d’image](#example-image)
-   [Exemple de Code](#sample-code)
-   [Propriétés d’effet](#effect-properties)
-   [Requirements](#requirements)
-   [Rubriques connexes](#related-topics)

## <a name="example-image"></a>Exemple d’image

![exemple de sortie d’effet](images/posterize-effect.png)

## <a name="sample-code"></a>Exemple de code


```C++
ComPtr<ID2D1Effect> posterizeEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Posterize, &posterizeEffect);
 
posterizeEffect->SetInput(0, bitmap);
posterizeEffect->SetValue(D2D1_POSTERIZE_PROP_RED_VALUE_COUNT, 4);
posterizeEffect->SetValue(D2D1_POSTERIZE_PROP_GREEN_VALUE_COUNT, 4);
posterizeEffect->SetValue(D2D1_POSTERIZE_PROP_BLUE_VALUE_COUNT, 4);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(posterizeEffect.Get());
m_d2dContext->EndDraw();


```



## <a name="effect-properties"></a>Propriétés d’effet

Les propriétés de l’effet Postérisation sont définies par l’énumération [**\_ \_ props d2d1**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_posterize_prop) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------------|---------------------------------------------------|
| Client minimal pris en charge | Windows 10 \[ applications de bureau \| Windows applications du windows Store\] |
| Serveur minimal pris en charge | Windows 10 \[ applications de bureau \| Windows applications du windows Store\] |
| En-tête                   | d2d1effects \_ 2. h                                  |
| Bibliothèque                  | d2d1. lib, dxguid. lib                              |

## <a name="related-topics"></a>Rubriques connexes

* [Interface ID2D1Effect](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)


