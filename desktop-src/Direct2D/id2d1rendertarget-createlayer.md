---
title: Méthodes ID2D1RenderTarget CreateLayer (D2d1. h)
description: Crée une ressource de couche qui peut être utilisée avec cette cible de rendu et ses cibles de rendu compatibles.
ms.assetid: 074e9ffb-c5f2-4e7b-94c7-d457bf07c0b7
keywords:
- Méthodes CreateLayer Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: a351c9e1b4fc36c816e87aeaae79a591bb43768a4e098bf315990fc1e1794fe4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120131489"
---
# <a name="id2d1rendertargetcreatelayer-methods"></a>ID2D1RenderTarget :: CreateLayer, méthodes

Crée une ressource de couche qui peut être utilisée avec cette cible de rendu et ses cibles de rendu compatibles.

### <a name="overload-list"></a>Liste de surcharge



| Méthode                                                                                                                 | Description                                                                                                                                                    |
|:-----------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateLayer (ID2D1Layer \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer))                                | Crée une ressource de couche qui peut être utilisée avec cette cible de rendu et ses cibles de rendu compatibles. <br/>                                               |
| [**CreateLayer (D2D1 \_ taille \_ F, ID2D1Layer \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(d2d1_size_f_id2d1layer))       | Crée une ressource de couche qui peut être utilisée avec cette cible de rendu et ses cibles de rendu compatibles. La nouvelle couche a la taille initiale spécifiée. <br/> |
| [**CreateLayer (D2D1 \_ taille \_ F \* , ID2D1Layer \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(d2d1_size_f_id2d1layer)) | Crée une ressource de couche qui peut être utilisée avec cette cible de rendu et ses cibles de rendu compatibles. La nouvelle couche a la taille initiale spécifiée. <br/> |



## <a name="remarks"></a>Remarques

La couche se redimensionne automatiquement, si nécessaire.

## <a name="examples"></a>Exemples

L’exemple suivant utilise une couche pour découper une image bitmap en un masque géométrique. Pour obtenir un exemple complet, consultez [Comment découper un masque géométrique](how-to-clip-with-layers.md).


```C++
HRESULT DemoApp::RenderWithLayer(ID2D1RenderTarget *pRT)
{
    HRESULT hr = S_OK;

    // Create a layer.
    ID2D1Layer *pLayer = NULL;
    hr = pRT->CreateLayer(NULL, &amp;pLayer);

    if (SUCCEEDED(hr))
    {
        pRT->SetTransform(D2D1::Matrix3x2F::Translation(350, 50));

        // Push the layer with the geometric mask.
        pRT->PushLayer(
            D2D1::LayerParameters(D2D1::InfiniteRect(), m_pPathGeometry),
            pLayer
            );
            
  
        pRT->DrawBitmap(m_pOrigBitmap, D2D1::RectF(0, 0, 200, 133));
        pRT->FillRectangle(D2D1::RectF(0.f, 0.f, 25.f, 25.f), m_pSolidColorBrush);  
        pRT->FillRectangle(D2D1::RectF(25.f, 25.f, 50.f, 50.f), m_pSolidColorBrush);
        pRT->FillRectangle(D2D1::RectF(50.f, 50.f, 75.f, 75.f), m_pSolidColorBrush); 
        pRT->FillRectangle(D2D1::RectF(75.f, 75.f, 100.f, 100.f), m_pSolidColorBrush);    
        pRT->FillRectangle(D2D1::RectF(100.f, 100.f, 125.f, 125.f), m_pSolidColorBrush); 
        pRT->FillRectangle(D2D1::RectF(125.f, 125.f, 150.f, 150.f), m_pSolidColorBrush);    
        

        pRT->PopLayer();
    }

    SafeRelease(&amp;pLayer);

    return hr;
}
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D2d1. h</dt> </dl>   |
| Bibliothèque<br/> | <dl> <dt>D2d1. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Vue d’ensemble des couches](direct2d-layers-overview.md)
</dt> <dt>

[**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> </dl>

�

�
