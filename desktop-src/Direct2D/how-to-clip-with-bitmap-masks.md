---
title: Utilisation d’une image bitmap comme masque d’opacité
description: Montre comment découper une région avec des masques bitmap.
ms.assetid: d6ad53a6-5e84-49d0-ab2c-5d6ad9428f9c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2106f43a6845cd724204fbf3e5aa1ec2b866bf46
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103941235"
---
# <a name="how-to-use-a-bitmap-as-an-opacity-mask"></a>Utilisation d’une image bitmap comme masque d’opacité

Cette rubrique explique comment utiliser une bitmap en tant que masque opacty en appelant la méthode [**ID2D1Factory :: FillOpacityMask**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillopacitymask(id2d1bitmap_id2d1brush_d2d1_opacity_mask_content_constd2d1_rect_f__constd2d1_rect_f_)) . Le masque d’opacité est une bitmap qui fournit les informations de couverture qui sont représentées par le canal alpha, qui contrôle la transparence du contenu rendu. Cette approche est plus efficace que l’utilisation de couches avec un masque d’opacité. Pour plus d’informations, consultez [vue d’ensemble des couches](direct2d-layers-overview.md).

**Pour découper une région**

1.  Chargez l’image bitmap d’origine à partir d’une ressource. Pour plus d’informations sur le chargement d’une image bitmap, consultez [Comment charger une image bitmap à partir d’une ressource](how-to-load-a-bitmap-from-a-resource.md).
2.  Chargez le masque de bitmap à partir d’une ressource.
3.  Créez un pinceau bitmap avec l’image bitmap d’origine. Pour plus d’informations sur la création d’un pinceau bitmap, consultez [How to Create a bitmap Brush](how-to-create-a-bitmap-brush.md).
4.  Appelez [**ID2D1Factory :: SetAntialiasMode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-setantialiasmode) pour définir le mode d’anticrénelage sur la cible de rendu sur le \_ mode d’anticrénelage d2d1 \_ \_ alias pour [**ID2D1Factory :: FillOpacityMask**](id2d1rendertarget-fillopacitymask.md) .
5.  Appelez [**FillOpacityMask**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillopacitymask(id2d1bitmap_id2d1brush_d2d1_opacity_mask_content_constd2d1_rect_f__constd2d1_rect_f_)) avec le masque bitmap et le pinceau bitmap sur la cible de rendu pour remplir le clip.

L’illustration suivante montre l’image bitmap d’origine sur la gauche, le masque de bitmap au centre et l’image bitmap découpée vers le masque à droite.

![illustration d’une image bitmap Goldfish, d’un masque en forme de poisson créé à partir de l’image bitmap et de l’image bitmap en forme de poisson qui en résulte après le masque](images/cliparegion-opacitymask.png)

Le code suivant montre comment découper la région avec le masque indiqué dans l’illustration précédente. Elle charge d’abord la bitmap d’origine et le masque bitmap. Puis crée un pinceau bitmap avec l’image bitmap d’origine.


```C++
// Create the bitmap to be used by the bitmap brush
if (SUCCEEDED(hr))
{
    hr = LoadResourceBitmap(
        m_pRenderTarget,
        m_pWICFactory,
        L"GoldFish",
        L"Image",
        &m_pOrigBitmap
        );
}

if (SUCCEEDED(hr))
{
    hr = LoadResourceBitmap(
        m_pRenderTarget,
        m_pWICFactory,
        L"GoldFishMask",
        L"Image",
        &m_pBitmapMask
        );
}

if (SUCCEEDED(hr))
{
    D2D1_BITMAP_BRUSH_PROPERTIES propertiesXClampYClamp = D2D1::BitmapBrushProperties(
        D2D1_EXTEND_MODE_CLAMP,
        D2D1_EXTEND_MODE_CLAMP,
        D2D1_BITMAP_INTERPOLATION_MODE_NEAREST_NEIGHBOR
        );

    hr = m_pRenderTarget->CreateBitmapBrush(
        m_pOrigBitmap,
        propertiesXClampYClamp,
        &m_pOriginalBitmapBrush
        );

    if (SUCCEEDED(hr))
    {
        hr = m_pRenderTarget->CreateBitmapBrush(
            m_pBitmapMask,
            propertiesXClampYClamp,
            &m_pBitmapMaskBrush
            );
    }
}
```



Il appelle ensuite [**SetAntialiasMode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-setantialiasmode) pour définir le mode d’anticrénelage. Appelez [**FillOpacityMask**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillopacitymask(id2d1bitmap_id2d1brush_d2d1_opacity_mask_content_constd2d1_rect_f__constd2d1_rect_f_)) pour utiliser un masque bitmap pour découper l’image bitmap d’origine.


```C++
// D2D1_ANTIALIAS_MODE_ALIASED must be set for FillOpacityMask
// to function properly.
m_pRenderTarget->SetAntialiasMode(D2D1_ANTIALIAS_MODE_ALIASED);

m_pRenderTarget->FillOpacityMask(
    m_pBitmapMask,
    m_pOriginalBitmapBrush,
    D2D1_OPACITY_MASK_CONTENT_GRAPHICS,
    &rcBrushRect,
    NULL
    );

m_pRenderTarget->SetAntialiasMode(D2D1_ANTIALIAS_MODE_PER_PRIMITIVE);

```



Pour plus d’informations sur les masques d’opacité, consultez [vue d’ensemble des masques d’opacité](opacity-masks-overview.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence Direct2D](reference.md)
</dt> </dl>

 

 