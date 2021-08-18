---
title: Effet de la netteté
description: Rend l’image plus nette.
ms.assetid: 1eb12d1e-83c1-ba13-33be-df2078f3ccb8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b74d95f7305dd6d44eb4dfbe2707f9e636e2ce704af2dc02fcf55477dbf2222d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119873762"
---
# <a name="sharpen-effect"></a>Effet de la netteté

Rend l’image plus nette.

Le CLSID de cet effet est CLSID \_ D2D1Sharpen.

-   [Exemple d’image](#example-image)
-   [Exemple de Code](#sample-code)
-   [Propriétés d’effet](#effect-properties)
-   [Requirements](#requirements)
-   [Rubriques connexes](#related-topics)

## <a name="example-image"></a>Exemple d’image

![exemple de sortie d’effet](images/sharpen-effect.png)

## <a name="sample-code"></a>Exemple de code


```C++
ComPtr<ID2D1Effect> sharpenEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Sharpen, &sharpenEffect);
 
sharpenEffect->SetInput(0, bitmap);
sharpenEffect->SetValue(D2D1_SHARPEN_PROP_SHARPNESS, 1.0f);
sharpenEffect->SetValue(D2D1_SHARPEN_PROP_THRESHOLD, 0.5f);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(hueToRgbEffect.Get());
m_d2dContext->EndDraw();


```



## <a name="effect-properties"></a>Propriétés d’effet

Les propriétés de l’effet de la netteté sont définies par l’énumération de la [**\_ \_ netteté d2d1**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_sharpen_prop) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------------|---------------------------------------------------|
| Client minimal pris en charge | Windows 10 \[ applications de bureau \| Windows applications du windows Store\] |
| Serveur minimal pris en charge | Windows 10 \[ applications de bureau \| Windows applications du windows Store\] |
| En-tête                   | d2d1effects \_ 2. h                                  |
| Bibliothèque                  | d2d1. lib, dxguid. lib                              |


## <a name="related-topics"></a>Rubriques connexes

* [Interface ID2D1Effect](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)



