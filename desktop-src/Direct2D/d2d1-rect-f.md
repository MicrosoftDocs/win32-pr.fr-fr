---
title: D2D1_RECT_F (D2DBaseTypes. h)
description: Représente un rectangle défini par les coordonnées de l’angle supérieur gauche (à gauche, en haut) et les coordonnées du coin inférieur droit (à droite, en bas). | D2D1_RECT_F (D2DBaseTypes. h)
ms.assetid: a961c0e3-fb76-4c07-b76e-47d8c09ada08
keywords:
- D2D1_RECT_F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93ce4700e093b9e82fd4334ae9e01485a7fcbb4c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104043006"
---
# <a name="d2d1_rect_f"></a>D2D1 \_ rect \_ F

Représente un rectangle défini par les coordonnées de l’angle supérieur gauche (à gauche, en haut) et les coordonnées du coin inférieur droit (à droite, en bas).


```C++
typedef D2D_RECT_F D2D1_RECT_F;
```



## <a name="remarks"></a>Notes

**D2d1 \_ RECT \_ f** est un nouveau nom pour le struct [**\_ rect \_ f de D2D**](/windows/desktop/api/dcommon/ns-dcommon-d2d_rect_f) déjà défini.

## <a name="examples"></a>Exemples

L’exemple suivant utilise un [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) pour dessiner et remplir plusieurs rectangles. Cet exemple produit une sortie comme indiqué dans l’illustration suivante.

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
        m_pRenderTarget->FillRectangle(&rectangle1, m_pLightSlateGrayBrush);

        // Draw the outline of a rectangle.
        m_pRenderTarget->DrawRectangle(&rectangle2, m_pCornflowerBlueBrush);

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

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 7, Windows Vista avec SP2 et mise à jour de la plateforme pour les applications de bureau Windows Vista, applications \[ \| UWP\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows Server 2008 R2, Windows Server 2008 avec SP2 et mise à jour de la plateforme pour les applications de bureau Windows Server 2008 pour applications \[ \| UWP\]<br/> |
| Téléphone minimal pris en charge<br/>  | Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 et applications Windows Runtime\]<br/>                                                  |
| En-tête<br/>                   | <dl> <dt>D2DBaseTypes. h (inclure D2d1. h)</dt> </dl>                               |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**D2D \_ rect \_ F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_rect_f)
</dt> <dt>

[Création d’une application Direct2D simple](direct2d-quickstart.md)
</dt> </dl>

 

