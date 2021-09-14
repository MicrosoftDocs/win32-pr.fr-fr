---
title: Effet clé Chroma
description: Convertit une couleur donnée plus ou moins une tolérance en alpha. Par exemple, la touche chroma peut supprimer l’arrière-plan d’une image pour un effet de recouvrement en vert à l’écran.
ms.assetid: f7bb5c65-f406-f947-c05d-2756cff99d21
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a13d5558d103d6f937ed6638d0debbeddaf71dd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127114157"
---
# <a name="chroma-key-effect"></a>Effet clé Chroma

Convertit une couleur donnée plus ou moins une tolérance en alpha. Par exemple, la touche chroma peut supprimer l’arrière-plan d’une image pour un effet de recouvrement en vert à l’écran.

Le CLSID de cet effet est CLSID \_ D2D1ChromaKey.

-   [Exemple d’image](#example-image)
-   [Exemple de Code](#sample-code)
-   [Propriétés d’effet](#effect-properties)
-   [Configuration requise](#requirements)
-   [Rubriques connexes](#related-topics)

## <a name="example-image"></a>Exemple d’image

![exemple de sortie d’effet](images/chromakey-effect.png)

> [!Note]  
> Dans cet exemple, la sortie de l’effet de clé Chroma est la deuxième image avec l’arrière-plan transparent de la damier. La troisième image combine cela avec une image d’arrière-plan pour la superposition finale de l’écran vert.

## <a name="sample-code"></a>Exemple de code

```cppcx
ComPtr<ID2D1Effect> chromakeyEffect;
m_d2dContext->CreateEffect(CLSID_D2D1ChromaKey, &chromakeyEffect);
 
chromakeyEffect->SetInput(0, bitmap);
chromaKeyEffect->SetValue(D2D1_CHROMAKEY_PROP_COLOR, {0.0f, 1.0f, 0.0f, 0.0f});
chromakeyEffect->SetValue(D2D1_CHROMAKEY_PROP_TOLERANCE, 0.2f);
chromakeyEffect->SetValue(D2D1_CHROMAKEY_PROP_INVERT_ALPHA, false);
chromakeyEffect->SetValue(D2D1_CHROMAKEY_PROP_FEATHER, false);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(chromakeyEffect.Get());
m_d2dContext->EndDraw();
```

## <a name="effect-properties"></a>Propriétés d’effet

Les propriétés de l’effet Chroma-Key sont définies par l’énumération [**d2d1 \_ CHROMAKEY \_ prop**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_chromakey_prop) .

## <a name="requirements"></a>Spécifications

| Condition requise | Valeur |
|--------------------------|---------------------------------------------------|
| Client minimal pris en charge | Windows 10 \[ applications de bureau \| Windows applications du windows Store\] |
| Serveur minimal pris en charge | Windows 10 \[ applications de bureau \| Windows applications du windows Store\] |
| En-tête                   | d2d1effects \_ 2. h                                  |
| Bibliothèque                  | d2d1. lib, dxguid. lib                              |

## <a name="related-topics"></a>Rubriques connexes

* [Interface ID2D1Effect](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
