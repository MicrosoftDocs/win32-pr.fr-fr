---
title: Comment dessiner une image bitmap
description: Montre comment afficher des bitmaps avec Direct2D.
ms.assetid: 9c6fc8b1-47ba-46fa-b812-2636cd8ff2b4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbfa13b75b4fe34ce6ff2b80598fac35f8483a2f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127113121"
---
# <a name="how-to-draw-a-bitmap"></a>Comment dessiner une image bitmap

Pour afficher un bitmap, utilisez la méthode [**ID2D1RenderTarget ::D rawbitmap**](id2d1rendertarget-drawbitmap.md) . L’exemple suivant montre comment utiliser la méthode **DrawBitmap** pour dessiner un [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap). Elle crée la sortie représentée dans l’illustration suivante.

![illustration d’une image bitmap d’origine et des bitmaps résultantes avec des paramètres et des transformations d’opacité différents](images/drawbitmapexample.png)

Tout d’abord, créez un [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap). L’exemple suivant charge une image bitmap à partir du fichier de ressources de l’application et la stocke sous la forme *m \_ pBitmap*. (Pour voir comment la `LoadResourceBitmap` méthode est implémentée, reportez-vous à [la rubrique chargement d’une image bitmap à partir d’une ressource](how-to-load-a-bitmap-from-a-resource.md).)


```C++
// Create a bitmap from an application resource.
hr = LoadResourceBitmap(
    m_pRenderTarget,
    m_pWICFactory,
    L"SampleImage",
    L"Image",
    200,
    0,
    &m_pBitmap
    );
```



Créez le [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) dans la même méthode que celle où vous avez créé la cible de rendu que vous allez utiliser pour dessiner la bitmap, puis libérez l’image bitmap lorsque la cible de rendu est libérée.

Une fois la bitmap créée, affichez-la. L’exemple suivant utilise la méthode [**DrawBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawbitmap(id2d1bitmap_constd2d1_rect_f_float_d2d1_bitmap_interpolation_mode_constd2d1_rect_f)) pour restituer une bitmap plusieurs fois à l’aide de différents paramètres de taille et d’opacité.


```C++
HRESULT DrawBitmapExample::OnRender()
{
    HRESULT hr;

    hr = CreateDeviceResources();

    if (SUCCEEDED(hr))
    {
        // Retrieve the size of the render target.
        D2D1_SIZE_F renderTargetSize = m_pRenderTarget->GetSize();

        m_pRenderTarget->BeginDraw();
        m_pRenderTarget->SetTransform(D2D1::Matrix3x2F::Identity());
        m_pRenderTarget->Clear(D2D1::ColorF(D2D1::ColorF::White));

        // Paint a grid background.
        m_pRenderTarget->FillRectangle(
            D2D1::RectF(0.0f, 0.0f, renderTargetSize.width, renderTargetSize.height),
            m_pGridPatternBitmapBrush
            );

        // Retrieve the size of the bitmap.
        D2D1_SIZE_F size = m_pBitmap->GetSize();

        D2D1_POINT_2F upperLeftCorner = D2D1::Point2F(100.f, 10.f);

        // Draw a bitmap.
        m_pRenderTarget->DrawBitmap(
            m_pBitmap,
            D2D1::RectF(
                upperLeftCorner.x,
                upperLeftCorner.y,
                upperLeftCorner.x + size.width,
                upperLeftCorner.y + size.height)
            );

        // Draw the next bitmap below the first one.
        upperLeftCorner.y = upperLeftCorner.y + size.height + 10.f;

        // Scale the bitmap to half its size using the linear
        // interoplation mode and draw it.
        float scaledWidth = size.width / 2.f;
        float scaledHeight = size.height / 2.f;
        m_pRenderTarget->DrawBitmap(
            m_pBitmap,
            D2D1::RectF(
                upperLeftCorner.x,
                upperLeftCorner.y,
                upperLeftCorner.x + scaledWidth,
                upperLeftCorner.y + scaledHeight),
            1.0,
            D2D1_BITMAP_INTERPOLATION_MODE_LINEAR
            );

        // Draw the bitmap at half its size and half its opacity.
        upperLeftCorner.y = upperLeftCorner.y + size.height / 2.f + 10.f;
        m_pRenderTarget->DrawBitmap(
            m_pBitmap,
            D2D1::RectF(
                upperLeftCorner.x,
                upperLeftCorner.y,
                upperLeftCorner.x + scaledWidth,
                upperLeftCorner.y + scaledHeight),
            0.5,
            D2D1_BITMAP_INTERPOLATION_MODE_LINEAR
            );

        // Draw a series of bitmaps with different opacity and
        // rotation angles.
        upperLeftCorner.y = upperLeftCorner.y + scaledHeight + 20.f;
        m_pRenderTarget->DrawBitmap(
            m_pBitmap,
            D2D1::RectF(
                upperLeftCorner.x,
                upperLeftCorner.y,
                upperLeftCorner.x + scaledWidth,
                upperLeftCorner.y + scaledHeight),
            0.5,
            D2D1_BITMAP_INTERPOLATION_MODE_LINEAR
            );

        D2D1_POINT_2F lowerLeftCorner = D2D1::Point2F(upperLeftCorner.x, upperLeftCorner.y + scaledHeight);
        D2D1_POINT_2F imageCenter = D2D1::Point2F(
            upperLeftCorner.x + scaledWidth / 2,
            upperLeftCorner.y + scaledHeight / 2
            );

        // Rotate the next bitmap by -20 degrees.
        m_pRenderTarget->SetTransform(
            D2D1::Matrix3x2F::Rotation(-20, imageCenter)
            );

        m_pRenderTarget->DrawBitmap(
            m_pBitmap,
            D2D1::RectF(
                upperLeftCorner.x,
                upperLeftCorner.y,
                upperLeftCorner.x + scaledWidth,
                upperLeftCorner.y + scaledHeight),
            0.75,
            D2D1_BITMAP_INTERPOLATION_MODE_LINEAR
            );

        m_pRenderTarget->SetTransform(
            D2D1::Matrix3x2F::Rotation(-45, imageCenter)
            );

        // Make the last bitmap fully opaque.
        m_pRenderTarget->DrawBitmap(
            m_pBitmap,
            D2D1::RectF(
                upperLeftCorner.x,
                upperLeftCorner.y,
                upperLeftCorner.x + scaledWidth,
                upperLeftCorner.y + scaledHeight),
            1.0,
            D2D1_BITMAP_INTERPOLATION_MODE_LINEAR
            );

        hr = m_pRenderTarget->EndDraw();

        if (hr == D2DERR_RECREATE_TARGET)
        {
            hr = S_OK;
            DiscardDeviceResources();
        }
    }

    return hr;
}
```



La méthode [**DrawBitmap**](id2d1rendertarget-drawbitmap.md) ne retourne pas de code d’erreur en cas d’échec. Pour déterminer si une opération de dessin (telle que **DrawBitmap**) a échoué, vérifiez le résultat retourné par la méthode [**ID2D1RenderTarget :: EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) , comme indiqué dans l’exemple suivant.


```C++
hr = m_pRenderTarget->EndDraw();
```



Le code a été omis de cet exemple.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**DrawBitmap**](id2d1rendertarget-drawbitmap.md)
</dt> <dt>

[**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap)
</dt> <dt>

[Chargement d’une image bitmap à partir d’une ressource](how-to-load-a-bitmap-from-a-resource.md)
</dt> </dl>

 

 