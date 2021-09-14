---
title: ID2D1RenderTarget DrawRectangle, méthodes (D2d1 \_ 1. h)
description: Dessine le contour d’un rectangle qui a les dimensions et le style de trait spécifiés.
ms.assetid: 3f8c0754-fa68-4b5b-812f-24d8b544ba6e
keywords:
- Méthodes DrawRectangle Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 4c1f846ca0bc1ddcb52696667edcb87291ae05df
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127112758"
---
# <a name="id2d1rendertargetdrawrectangle-methods"></a>ID2D1RenderTarget ::D méthodes rawRectangle

Dessine le contour d’un rectangle qui a les dimensions et le style de trait spécifiés.

### <a name="overload-list"></a>Liste de surcharge



| Méthode                                                                                                                                                                   | Description                                                                                      |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------|
| [**DrawRectangle (D2D1 \_ rect \_ F&, ID2D1Brush \* , float, ID2D1StrokeStyle \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle))  | Dessine le contour d’un rectangle qui a les dimensions et le style de trait spécifiés. <br/> |
| [**DrawRectangle (D2D1 \_ rect \_ F \* , ID2D1Brush \* , float, ID2D1StrokeStyle \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle)) | Dessine le contour d’un rectangle qui a les dimensions et le style de trait spécifiés. <br/> |



## <a name="remarks"></a>Notes

Lorsque cette méthode échoue, elle ne retourne pas de code d’erreur. Pour déterminer si une méthode de dessin (par exemple, **DrawRectangle**) a échoué, vérifiez le résultat retourné par la méthode [**ID2D1RenderTarget :: EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) ou [**ID2D1RenderTarget :: Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) .

## <a name="examples"></a>Exemples

L’exemple suivant utilise un [**ID2D1HwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85)) pour dessiner et remplir plusieurs rectangles. Cet exemple produit la sortie représentée dans l’illustration suivante.

![illustration de deux rectangles sur un arrière-plan de grille](images/drawrectangleexample-small.png)


```C++
// This method discards device-specific
// resources if the Direct3D device dissapears during execution and
// recreates the resources the next time it's invoked.
HRESULT DemoApp::OnRender()
{
    HRESULT hr = S_OK;

    hr = CreateDeviceResources();

    if (SUCCEEDED(hr))
    {
        m_pRenderTarget->BeginDraw();

        m_pRenderTarget->SetTransform(D2D1::Matrix3x2F::Identity());

        m_pRenderTarget->Clear(D2D1::ColorF(D2D1::ColorF::White));

        D2D1_SIZE_F rtSize = m_pRenderTarget->GetSize();

        // Draw a grid background.
        int width = static_cast<int>(rtSize.width);
        int height = static_cast<int>(rtSize.height);

        for (int x = 0; x < width; x += 10)
        {
            m_pRenderTarget->DrawLine(
                D2D1::Point2F(static_cast<FLOAT>(x), 0.0f),
                D2D1::Point2F(static_cast<FLOAT>(x), rtSize.height),
                m_pLightSlateGrayBrush,
                0.5f
                );
        }

        for (int y = 0; y < height; y += 10)
        {
            m_pRenderTarget->DrawLine(
                D2D1::Point2F(0.0f, static_cast<FLOAT>(y)),
                D2D1::Point2F(rtSize.width, static_cast<FLOAT>(y)),
                m_pLightSlateGrayBrush,
                0.5f
                );
        }

        // Draw two rectangles.
        D2D1_RECT_F rectangle1 = D2D1::RectF(
            rtSize.width/2 - 50.0f,
            rtSize.height/2 - 50.0f,
            rtSize.width/2 + 50.0f,
            rtSize.height/2 + 50.0f
            );

        D2D1_RECT_F rectangle2 = D2D1::RectF(
            rtSize.width/2 - 100.0f,
            rtSize.height/2 - 100.0f,
            rtSize.width/2 + 100.0f,
            rtSize.height/2 + 100.0f
            );


        // Draw a filled rectangle.
        m_pRenderTarget->FillRectangle(&amp;rectangle1, m_pLightSlateGrayBrush);

        // Draw the outline of a rectangle.
        m_pRenderTarget->DrawRectangle(&amp;rectangle2, m_pCornflowerBlueBrush);

        hr = m_pRenderTarget->EndDraw();
    }

    if (hr == D2DERR_RECREATE_TARGET)
    {
        hr = S_OK;
        DiscardDeviceResources();
    }

    return hr;
}
```



Pour obtenir un didacticiel connexe, consultez [création d’une application Direct2D simple](direct2d-quickstart.md).

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

[Création d’une application Direct2D simple](direct2d-quickstart.md)
</dt> <dt>

[Comment dessiner et remplir une forme de base](how-to-draw-an-ellipse.md)
</dt> </dl>

�

�
