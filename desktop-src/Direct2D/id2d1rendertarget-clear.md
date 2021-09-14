---
title: ID2D1RenderTarget méthodes Clear
description: Efface la zone de dessin à la couleur spécifiée.
ms.assetid: 3bfec923-17fc-479a-a760-9baab2ff3a56
keywords:
- Effacer les méthodes Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: 346e44e3ce0b59e40577d3207f45faafdc33b367
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127112805"
---
# <a name="id2d1rendertargetclear-methods"></a>ID2D1RenderTarget :: Clear, méthodes

Efface la zone de dessin à la couleur spécifiée.

### <a name="overload-list"></a>Liste de surcharge



| Méthode                                                                 | Description                                                 |
|:-----------------------------------------------------------------------|:------------------------------------------------------------|
| [**Clear ( \_ couleur d2d1 \_ F \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-clear(constd2d1_color_f)) | Efface la zone de dessin à la couleur spécifiée. <br/> |
| [**Clear ( \_ couleur d2d1 \_ F&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-clear(constd2d1_color_f_))  | Efface la zone de dessin à la couleur spécifiée. <br/> |



## <a name="remarks"></a>Notes

Direct2D interprète le *clearColor* comme étant directement alpha (non prémultiplié). Si le mode Alpha de la cible de rendu est [**d2d1 \_ alpha \_ mode \_ ignore**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode), le canal alpha de *clearColor* est ignoré et remplacé par 1,0 f (entièrement opaque).

Si la cible de rendu a un clip actif (spécifié par [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode))), la commande Effacer est appliquée uniquement à la zone dans la zone de découpage.

## <a name="examples"></a>Exemples

L’exemple suivant utilise la méthode **Clear** pour créer un arrière-plan blanc avant de restituer un autre contenu.


```C++
//  Called whenever the application needs to display the client
//  window. This method writes "Hello, World"
//
//  Note that this function will automatically discard device-specific
//  resources if the Direct3D device disappears during function
//  invocation, and will recreate the resources the next time it's
//  invoked.
//
HRESULT DemoApp::OnRender()
{
    HRESULT hr;

    hr = CreateDeviceResources();

    if (SUCCEEDED(hr))
    {
        static const WCHAR sc_helloWorld[] = L"Hello, World!";

        // Retrieve the size of the render target.
        D2D1_SIZE_F renderTargetSize = m_pRenderTarget->GetSize();

        m_pRenderTarget->BeginDraw();

        m_pRenderTarget->SetTransform(D2D1::Matrix3x2F::Identity());

        m_pRenderTarget->Clear(D2D1::ColorF(D2D1::ColorF::White));

        m_pRenderTarget->DrawText(
            sc_helloWorld,
            ARRAYSIZE(sc_helloWorld) - 1,
            m_pTextFormat,
            D2D1::RectF(0, 0, renderTargetSize.width, renderTargetSize.height),
            m_pBlackBrush
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



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|-------------------------------------------------------------------------------------|
| Bibliothèque<br/> | <dl> <dt>D2d1. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> </dl>

 

