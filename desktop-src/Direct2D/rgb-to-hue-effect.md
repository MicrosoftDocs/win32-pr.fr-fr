---
title: Effet RGB-à-teinte
description: Convertit une image RVB en espaces de couleurs TSL (teinte, saturation, luminosité) ou HSV (teinte, saturation, valeur).
ms.assetid: 1def972d-8172-9217-8ce7-abce4a93f6e1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c474705d050c2ef2eff9050a759c60c5d8f1098440e06601ec1e3981e349aaff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118160385"
---
# <a name="rgb-to-hue-effect"></a>Effet RGB-à-teinte

Convertit une image RVB en espaces de couleurs TSL (teinte, saturation, luminosité) ou HSV (teinte, saturation, valeur).

TSL et HSV sont deux modèles différents pour représenter une couleur RVB dans un espace colorimétrique cylindrique. Ils sont utiles car ils vous permettent d’obtenir des informations sur une couleur à l’aide de concepts plus intuitifs, tels que la teinte et l’intensité, et la combinaison de valeurs rouge, vert et bleu.

Cet effet normalise les données de sortie (valeur de teinte, de saturation pour HSV ou teinte, saturation, luminosité pour TSL) à la plage \[ 0, 1 \] .

Le CLSID de cet effet est CLSID \_ D2D1RgbToHue.

Pour inverser le comportement de cet effet, utilisez l' [effet teinter au RVB](hue-to-rgb-effect.md).

-   [Exemple de Code](#sample-code)
-   [Propriétés d’effet](#effect-properties)
-   [Requirements](#requirements)
-   [Rubriques connexes](#related-topics)

## <a name="sample-code"></a>Exemple de code


```C++
ComPtr<ID2D1Effect> rgbToHueEffect;
m_d2dContext->CreateEffect(CLSID_D2D1RgbToHue, &rgbToHueEffect);
 
rgbToHueEffect->SetInput(0, bitmap);
rgbToHueEffect->SetValue(D2D1_RGBTOHUE_PROP_OUTPUT_COLOR_SPACE, D2D1_RGBTOHUE_OUTPUT_COLOR_SPACE_HUE_SATURATION_VALUE);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(rgbToHueEffect.Get());
m_d2dContext->EndDraw();

```



## <a name="effect-properties"></a>Propriétés d’effet

Les propriétés de l’effet de contraste sont définies par l’énumération [**d2d1 \_ RGBTOHUE \_ prop**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_rgbtohue_prop) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------------|---------------------------------------------------|
| Client minimal pris en charge | Windows 10 \[ applications de bureau \| Windows applications du windows Store\] |
| Serveur minimal pris en charge | Windows 10 \[ applications de bureau \| Windows applications du windows Store\] |
| En-tête                   | d2d1effects \_ 2. h                                  |
| Bibliothèque                  | d2d1. lib, dxguid. lib                              |


## <a name="related-topics"></a>Rubriques connexes

* [Interface ID2D1Effect](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
