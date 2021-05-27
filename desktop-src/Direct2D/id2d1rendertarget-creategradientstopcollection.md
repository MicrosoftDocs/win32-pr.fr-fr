---
title: Méthodes ID2D1RenderTarget CreateGradientStopCollection (D2d1 \_ 1. h)
description: Crée un ID2D1GradientStopCollection à partir du tableau spécifié de \_ structures de point de dégradé d2d1 \_ .
ms.assetid: 674ffba5-18c5-46bf-8813-d8d13e5ba903
keywords:
- Méthodes CreateGradientStopCollection Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: f099c1c71015ca433299843d388085103571d31d
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549414"
---
# <a name="id2d1rendertargetcreategradientstopcollection-methods"></a>ID2D1RenderTarget :: CreateGradientStopCollection, méthodes

Crée un [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) à partir du tableau spécifié de structures de [**\_ \_ point de dégradé d2d1**](/windows/win32/api/d2d1/ns-d2d1-d2d1_gradient_stop) .

### <a name="overload-list"></a>Liste de surcharge



| Méthode                                                                                                                                                                                                                                                               | Description                                                                                                                                                                                                                           |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateGradientStopCollection (D2D1 \_ \_ Stop \* , D2D1 \_ gamma, d2d1 \_ mode Extend \_ , ID2D1GradientStopCollection \* \* )**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) | Crée un [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) à partir des points de dégradé, du gamma d’interpolation de couleur et du mode extension spécifiés. <br/>                                                              |
| [**CreateGradientStopCollection (D2D1 \_ point \_ \* de dégradé, ID2D1GradientStopCollection \* \* )**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection)                                                            | Crée un [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) à partir des points de dégradé spécifiés qui utilisent la gamma de l’interpolation de couleur [**d2d1 \_ gamma \_ 2 \_ 2**](/windows/win32/api/d2d1/ne-d2d1-d2d1_gamma) et le mode d’extension de la bride.<br/> |



## <a name="examples"></a>Exemples

L’exemple suivant crée un tableau de points de dégradé, puis les utilise pour créer un [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection).


```C++
// Create an array of gradient stops to put in the gradient stop
// collection that will be used in the gradient brush.
ID2D1GradientStopCollection *pGradientStops = NULL;

D2D1_GRADIENT_STOP gradientStops[2];
gradientStops[0].color = D2D1::ColorF(D2D1::ColorF::Yellow, 1);
gradientStops[0].position = 0.0f;
gradientStops[1].color = D2D1::ColorF(D2D1::ColorF::ForestGreen, 1);
gradientStops[1].position = 1.0f;
// Create the ID2D1GradientStopCollection from a previously
// declared array of D2D1_GRADIENT_STOP structs.
hr = m_pRenderTarget->CreateGradientStopCollection(
    gradientStops,
    2,
    D2D1_GAMMA_2_2,
    D2D1_EXTEND_MODE_CLAMP,
    &pGradientStops
    );
```



L’exemple de code suivant utilise [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) pour créer un [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush).


```C++
// The line that determines the direction of the gradient starts at
// the upper-left corner of the square and ends at the lower-right corner.

if (SUCCEEDED(hr))
{
    hr = m_pRenderTarget->CreateLinearGradientBrush(
        D2D1::LinearGradientBrushProperties(
            D2D1::Point2F(0, 0),
            D2D1::Point2F(150, 150)),
        pGradientStops,
        &m_pLinearGradientBrush
        );
}
```



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|-------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D2d1 \_ 1. h (inclure D2d1. h)</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D2d1. lib</dt> </dl>                   |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl>                   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

[**\_Point de dégradé d2d1 \_**](/windows/win32/api/d2d1/ns-d2d1-d2d1_gradient_stop)
</dt> <dt>

[Comment créer un pinceau de dégradé linéaire](how-to-create-a-linear-gradient-brush.md)
</dt> <dt>

[Comment créer un pinceau de dégradé radial](how-to-create-a-radial-gradient-brush.md)
</dt> <dt>

[Vue d’ensemble des pinceaux](direct2d-brushes-overview.md)
</dt> </dl>