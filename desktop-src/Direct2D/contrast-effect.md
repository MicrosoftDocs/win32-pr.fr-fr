---
title: Effet de contraste
description: augmente ou diminue le contraste d’une image.
ms.assetid: c0cc0f86-f6d4-e951-0cdd-dbad488e0793
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6f287b1309aceadc4709bae3b1c2101a06df32d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032968"
---
# <a name="contrast-effect"></a>Effet de contraste

augmente ou diminue le contraste d’une image.

Le CLSID de cet effet est CLSID \_ D2D1Contrast.

La fonction Contrast modifie chaque valeur de canal de couleur à l’aide de deux degrés polynomiaux par morceaux quadratiques qui satisfont à la continuité de pente au point (0,5, 0,5).

![par morceaux quadratiques polynomiaux qui remplissent la continuité de pente au point (0,5, 0,5)](images/contrast-effect-slope.png)

-   [Exemples d’images](#example-images)
-   [Exemple de Code](#sample-code)
-   [Propriétés d’effet](#effect-properties)
-   [Configuration requise](#requirements)
-   [Rubriques connexes](#related-topics)

## <a name="example-images"></a>Exemples d’images

Cet exemple montre la sortie de l’effet avec le contraste maximal appliqué (contraste = 1,0).

Avant

![l’image avant l’effet est appliquée](images/contrast-effect-before.png)

After

![une image après l’effet est appliquée](images/contrast-effect-after.png)

## <a name="sample-code"></a>Exemple de code

```cpp
ComPtr<ID2D1Effect> contrastEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Contrast, &contrastEffect);
 
contrastEffect->SetInput(0, bitmap);
contrastEffect->SetValue(D2D1_CONTRAST_PROP_CONTRAST, 0.5f);
contrastEffect->SetValue(D2D1_CONTRAST_PROP_CLAMP_INPUT, TRUE);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(contrastEffect.Get());
m_d2dContext->EndDraw();
```

## <a name="effect-properties"></a>Propriétés d’effet

Les propriétés de l’effet de contraste sont définies par l’énumération de la propriété de [**\_ \_ contraste d2d1**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_contrast_prop) .

## <a name="requirements"></a>Configuration requise

| Condition requise | Valeur |
|--------------------------|---------------------------------------------------|
| Client minimal pris en charge | Applications de \[ Bureau Windows 10 \| applications du Windows Store\] |
| Serveur minimal pris en charge | Applications de \[ Bureau Windows 10 \| applications du Windows Store\] |
| En-tête                   | d2d1effects \_ 2. h                                  |
| Bibliothèque                  | d2d1. lib, dxguid. lib                              |

## <a name="related-topics"></a>Rubriques connexes

* [Interface ID2D1Effect](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
