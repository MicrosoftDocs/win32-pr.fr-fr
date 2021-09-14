---
title: Effet teinte-à-RGB
description: Convertit une image TSL (teinte, saturation, luminosité) ou HSV (teinte, saturation, valeur) en un espace de couleurs RVB.
ms.assetid: 18e92535-9e89-bf8d-b8c3-a49b645fc417
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82064d01281ab0edf2327f00cf6e852a0bebae53
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127113066"
---
# <a name="hue-to-rgb-effect"></a>Effet teinte-à-RGB

Convertit une image TSL (teinte, saturation, luminosité) ou HSV (teinte, saturation, valeur) en un espace de couleurs RVB.

TSL et HSV sont deux modèles différents pour représenter une couleur RVB dans un espace colorimétrique cylindrique. Ils sont utiles car ils vous permettent d’obtenir des informations sur une couleur à l’aide de concepts plus intuitifs, tels que la teinte et l’intensité, et la combinaison de valeurs rouge, vert et bleu.

Cet effet passe par toutes les valeurs alpha d’entrée.

Le CLSID de cet effet est CLSID \_ D2D1HueToRgb.

Pour inverser le comportement de cet effet, utilisez l' [effet RVB pour teinte](rgb-to-hue-effect.md).

-   [Exemple de Code](#sample-code)
-   [Propriétés d’effet](#effect-properties)
-   [Configuration requise](#requirements)
-   [Rubriques connexes](#related-topics)

## <a name="sample-code"></a>Exemple de code

```cpp
ComPtr<ID2D1Effect> hueToRgbEffect;
m_d2dContext->CreateEffect(CLSID_D2D1HueToRgb, &hueToRgbEffect);
 
hueToRgbEffect->SetInput(0, bitmap);
hueToRgbEffect->SetValue(D2D1_HUETORGB_INPUT_COLOR_SPACE, D2D1_HUETORGB_INPUT_COLOR_SPACE_HUE_SATURATION_LIGHTNESS);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(hueToRgbEffect.Get());
m_d2dContext->EndDraw();
```

## <a name="effect-properties"></a>Propriétés d’effet

Les propriétés de l’effet de contraste sont définies par l’énumération [**d2d1 \_ HUETORGB \_ prop**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_huetorgb_prop) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------------|---------------------------------------------------|
| Client minimal pris en charge | Windows 10 \[ applications de bureau \| Windows applications du windows Store\] |
| Serveur minimal pris en charge | Windows 10 \[ applications de bureau \| Windows applications du windows Store\] |
| En-tête                   | d2d1effects \_ 2. h                                  |
| Bibliothèque                  | d2d1. lib, dxguid. lib                              |



## <a name="related-topics"></a>Rubriques connexes

* [Interface ID2D1Effect](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
