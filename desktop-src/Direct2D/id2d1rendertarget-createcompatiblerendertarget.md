---
title: Méthodes ID2D1RenderTarget CreateCompatibleRenderTarget (D2d1. h)
description: Crée une cible de rendu bitmap à utiliser pendant le dessin intermédiaire hors écran qui est compatible avec la cible de rendu actuelle.
ms.assetid: 4a799a7c-0d2f-460f-99f9-24c6cf7c4537
keywords:
- Méthodes CreateCompatibleRenderTarget Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 0f0de8478d2ab3ee2e7142bd0e197053dc58ac2a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127112797"
---
# <a name="id2d1rendertargetcreatecompatiblerendertarget-methods"></a>ID2D1RenderTarget :: CreateCompatibleRenderTarget, méthodes

Crée une cible de rendu bitmap à utiliser pendant le dessin intermédiaire hors écran qui est compatible avec la cible de rendu actuelle.

### <a name="overload-list"></a>Liste de surcharge



| Méthode                                                                                                                                                                                                                        | Description                                                                                                                                                                                                                                            |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateCompatibleRenderTarget (D2D1 \_ taille \_ F, d2d1 \_ taille \_ U, \_ format de pixel d2d1 \_ , \_ options de \_ cible de rendu compatibles d2d1 \_ \_ , ID2D1BitmapRenderTarget \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createcompatiblerendertarget(d2d1_size_f_d2d1_size_u_d2d1_pixel_format_d2d1_compatible_render_target_options_id2d1bitmaprendertarget))       | Crée une cible de rendu bitmap à utiliser pendant un dessin intermédiaire hors écran qui est compatible avec la cible de rendu actuelle.<br/>                                                                                                             |
| [**CreateCompatibleRenderTarget (D2D1 \_ taille \_ F \* , d2d1 \_ taille \_ U \* , \_ format de pixel d2d1 \_ \* , \_ options de \_ cible de rendu compatibles d2d1 \_ \_ , ID2D1BitmapRenderTarget \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createcompatiblerendertarget(d2d1_size_f_d2d1_size_u_d2d1_pixel_format_d2d1_compatible_render_target_options_id2d1bitmaprendertarget)) | Crée une cible de rendu bitmap à utiliser pendant un dessin intermédiaire hors écran qui est compatible avec la cible de rendu actuelle. <br/>                                                                                                            |
| [**CreateCompatibleRenderTarget (ID2D1BitmapRenderTarget \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createcompatiblerendertarget(id2d1bitmaprendertarget))                                                                                                 | Crée une cible de rendu bitmap à utiliser pendant le dessin intermédiaire hors écran qui est compatible avec la cible de rendu actuelle et a les mêmes taille, PPP et format de pixel (mais pas le mode Alpha) que la cible de rendu actuelle. <br/>         |
| [**CreateCompatibleRenderTarget (D2D1 \_ taille \_ F, ID2D1BitmapRenderTarget \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createcompatiblerendertarget(d2d1_size_f_id2d1bitmaprendertarget))                                                                                   | Crée une cible de rendu bitmap à utiliser pendant le dessin intermédiaire hors écran qui est compatible avec la cible de rendu actuelle et qui a le même format de pixel (mais pas le mode Alpha) que la cible de rendu actuelle. <br/>                        |
| [**CreateCompatibleRenderTarget (D2D1 \_ taille \_ F, d2d1 \_ taille \_ U, ID2D1BitmapRenderTarget \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createcompatiblerendertarget(d2d1_size_f_d2d1_size_u_id2d1bitmaprendertarget))                                                                     | Crée une cible de rendu bitmap à utiliser pendant le dessin intermédiaire hors écran qui est compatible avec la cible de rendu actuelle. La nouvelle cible de rendu bitmap a le même format de pixel (mais pas le mode Alpha) que la cible de rendu actuelle. <br/> |
| [**CreateCompatibleRenderTarget (D2D1 \_ size \_ F, d2d1 \_ size \_ U, d2d1 \_ pixel \_ format, ID2D1BitmapRenderTarget \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createcompatiblerendertarget(d2d1_size_f_d2d1_size_u_d2d1_pixel_format_id2d1bitmaprendertarget))                                                 | Crée une cible de rendu bitmap à utiliser pendant un dessin intermédiaire hors écran qui est compatible avec la cible de rendu actuelle. <br/>                                                                                                            |



## <a name="examples"></a>Exemples

L’exemple suivant utilise la méthode **CreateCompatibleRenderTarget** pour créer un [**ID2D1BitmapRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmaprendertarget) et l’utilise pour dessiner un modèle de grille. Le modèle de grille est utilisé comme source d’un [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush).


```C++
HRESULT DemoApp::CreateGridPatternBrush(
    ID2D1RenderTarget *pRenderTarget,
    ID2D1BitmapBrush **ppBitmapBrush
    )
{
    // Create a compatible render target.
    ID2D1BitmapRenderTarget *pCompatibleRenderTarget = NULL;
    HRESULT hr = pRenderTarget->CreateCompatibleRenderTarget(
        D2D1::SizeF(10.0f, 10.0f),
        &amp;pCompatibleRenderTarget
        );
    if (SUCCEEDED(hr))
    {
        // Draw a pattern.
        ID2D1SolidColorBrush *pGridBrush = NULL;
        hr = pCompatibleRenderTarget->CreateSolidColorBrush(
            D2D1::ColorF(D2D1::ColorF(0.93f, 0.94f, 0.96f, 1.0f)),
            &amp;pGridBrush
            );
        if (SUCCEEDED(hr))
        {
            pCompatibleRenderTarget->BeginDraw();
            pCompatibleRenderTarget->FillRectangle(D2D1::RectF(0.0f, 0.0f, 10.0f, 1.0f), pGridBrush);
            pCompatibleRenderTarget->FillRectangle(D2D1::RectF(0.0f, 0.1f, 1.0f, 10.0f), pGridBrush);
            pCompatibleRenderTarget->EndDraw();

            // Retrieve the bitmap from the render target.
            ID2D1Bitmap *pGridBitmap = NULL;
            hr = pCompatibleRenderTarget->GetBitmap(&amp;pGridBitmap);
            if (SUCCEEDED(hr))
            {
                // Choose the tiling mode for the bitmap brush.
                D2D1_BITMAP_BRUSH_PROPERTIES brushProperties =
                    D2D1::BitmapBrushProperties(D2D1_EXTEND_MODE_WRAP, D2D1_EXTEND_MODE_WRAP);

                // Create the bitmap brush.
                hr = m_pRenderTarget->CreateBitmapBrush(pGridBitmap, brushProperties, ppBitmapBrush);

                pGridBitmap->Release();
            }

            pGridBrush->Release();
        }

        pCompatibleRenderTarget->Release();
    }

    return hr;
}
```



L’exemple de code suivant utilise le pinceau pour peindre un modèle.


```C++
// Paint a grid background.
m_pRenderTarget->FillRectangle(
    D2D1::RectF(0.0f, 0.0f, renderTargetSize.width, renderTargetSize.height),
    m_pGridPatternBitmapBrush
    );
```



Le code a été omis de cet exemple.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|-------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D2d1. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>D2d1. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> </dl>

�

�
