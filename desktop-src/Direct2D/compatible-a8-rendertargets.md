---
title: Vue d’ensemble des cibles de rendu a8 compatibles
description: Décrit les principes de base des cibles de rendu a8 compatibles et fournit des exemples montrant comment les utiliser.
ms.assetid: 218c0123-8da9-4d73-9882-cbf7f205001f
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 552577283adfa9a440e94b7e04f4056bd6c3ecda
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/18/2020
ms.locfileid: "103941531"
---
# <a name="compatible-a8-render-targets-overview"></a>Vue d’ensemble des cibles de rendu a8 compatibles

Cette rubrique décrit les principes de base d’une cible de rendu a8 compatible et fournit des exemples d’utilisation de celle-ci.

Une cible de rendu a8 compatible est une cible de rendu compatible ([**ID2D1BitmapRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmaprendertarget)) qui utilise un format de pixel A8 ( \_ format dxgi \_ a8 \_ UNORM). Vous pouvez utiliser une cible de rendu a8 compatible pour améliorer les performances de l’application et fournir des transitions plus lisses pendant l’animation de texte. Une cible de rendu a8 compatible est particulièrement utile lorsque vous essayez d’améliorer les éléments suivants :

-   Fréquence d’images de l’application qui restitue le texte ou la géométrie avec anticrénelage qui comprend uniquement des animations simples, telles que des modifications de translation, de rotation, de mise à l’échelle ou de couleur.

-   Continuité visuelle de l’application qui étire et diminshes le texte pendant une animation.

Pour créer une cible de rendu a8 compatible, utilisez la méthode [**ID2D1RenderTarget :: CreateCompatibleRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createcompatiblerendertarget(id2d1bitmaprendertarget)) avec le format \_ dxgi \_ a8 \_ UNORM pixel format et spécifiez une cible de rendu compatible retournée. Pour plus d’informations sur les formats de pixel, consultez [formats de pixel pris en charge et modes alpha](./supported-pixel-formats-and-alpha-modes.md).

Par exemple, pour animer efficacement le texte affiché dans la capture d’écran suivante, utilisez une cible de rendu a8 compatible pour mettre en cache le texte en tant que masque d’opacité. Ensuite, appliquez des transformations au masque d’opacité pour obtenir des résultats de rendu rapides.

![capture d’écran du texte à animer](images/a8rendertarget.png)

Le code suivant montre comment procéder. Elle crée une cible de rendu a8 compatible, récupère la bitmap à partir de celle-ci, puis restitue la bitmap à l’aide de [**FillOpacityMask**](id2d1rendertarget-fillopacitymask.md).

```cpp
ID2D1BitmapRenderTarget *m_pOpacityRT;

// Create the compatible render target using desiredPixelSize to avoid
// blurriness issues caused by a fractional-pixel desiredSize.

D2D1_PIXEL_FORMAT alphaOnlyFormat = D2D1::PixelFormat(
    DXGI_FORMAT_A8_UNORM, 
    D2D1_ALPHA_MODE_PREMULTIPLIED);

hr = m_pRT->CreateCompatibleRenderTarget(
    NULL,
    &maskPixelSize,
    &alphaOnlyFormat,
    D2D1_COMPATIBLE_RENDER_TARGET_OPTIONS_NONE,
    &m_pOpacityRT
    );

D2D1_RECT_F destinationRect = D2D1::RectF(
    roundedOffset.x,
    roundedOffset.y,
    roundedOffset.x + opacityRTSize.width,
    roundedOffset.y + opacityRTSize.height
    );

ID2D1Bitmap *pBitmap = NULL;
m_pOpacityRT->GetBitmap(&pBitmap);

pBitmap->GetDpi(&dpiX, &dpiY);

// The antialias mode must be set to D2D1_ANTIALIAS_MODE_ALIASED
// for this method to succeed. We've set this mode already though
// so no need to do it again.

m_pRT->FillOpacityMask(
    pBitmap,
    m_pBlackBrush,
    D2D1_OPACITY_MASK_CONTENT_TEXT_NATURAL,
    &destinationRect
    );

pBitmap->Release();
```

## <a name="related-topics"></a>Rubriques connexes

[Référence Direct2D](reference.md)