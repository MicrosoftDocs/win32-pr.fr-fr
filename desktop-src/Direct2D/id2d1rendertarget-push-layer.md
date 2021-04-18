---
title: Méthodes ID2D1RenderTarget PushLayer (D2d1 \_ 1. h)
description: Ajoute la couche spécifiée à la cible de rendu afin qu’elle reçoive toutes les opérations de dessin suivantes jusqu’à ce que PopLayer soit appelé.
ms.assetid: 9336662c-e94e-40ba-adbe-066d704958bc
keywords:
- Méthodes PushLayer Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 6a5609192162ae0b0c0e2af8f1b84429d8710509
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533484"
---
# <a name="id2d1rendertargetpushlayer-methods"></a>ID2D1RenderTarget ::P méthodes ushLayer

Ajoute la couche spécifiée à la cible de rendu afin qu’elle reçoive toutes les opérations de dessin suivantes jusqu’à ce que [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) soit appelé.

### <a name="overload-list"></a>Liste de surcharge



| Méthode                                                                                                                            | Description                                                                                                                                                                     |
|:----------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PushLayer (paramètres de la \_ couche D2D1 \_&, ID2D1Layer \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer))  | Ajoute la couche spécifiée à la cible de rendu afin qu’elle reçoive toutes les opérations de dessin suivantes jusqu’à ce que [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) soit appelé. <br/> |
| [**PushLayer ( \_ paramètres de couche d2d1 \_ \* , ID2D1Layer \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters_id2d1layer)) | Ajoute la couche spécifiée à la cible de rendu afin qu’elle reçoive toutes les opérations de dessin suivantes jusqu’à ce que [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) soit appelé. <br/> |



## <a name="remarks"></a>Notes

La méthode [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) permet à un appelant de commencer à rediriger le rendu vers une couche. Toutes les opérations de rendu sont valides dans une couche. L’emplacement de la couche est affecté par le jeu de transformations universelles sur la cible de rendu.

Chaque **PushLayer** doit avoir un appel [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) correspondant. S’il y a plus d’appels **PopLayer** que d’appels **PushLayer** , la cible de rendu est placée dans un état d’erreur. Si [**flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) est appelé avant que toutes les couches en suspens soient dépilées, la cible de rendu est placée dans un état d’erreur et une erreur est retournée. L’état d’erreur peut être effacé par un appel à [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw).

Une ressource [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) particulière ne peut être active qu’en même temps. En d’autres termes, vous ne pouvez pas appeler une méthode [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) , puis suivre immédiatement une autre méthode **PushLayer** avec la même ressource de couche. Au lieu de cela, vous devez appeler la deuxième méthode **PushLayer** avec des ressources de couche différentes.

Pour obtenir un exemple, consultez [Comment découper une région avec des couches](how-to-clip-with-layers.md).

Cette méthode ne retourne pas de code d’erreur en cas d’échec. Pour déterminer si une opération de dessin (telle que **PushLayer**) a échoué, vérifiez le résultat retourné par les méthodes [**ID2D1RenderTarget :: EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) ou [**ID2D1RenderTarget :: Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) .

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
|--------------------|-------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>D2d1 \_ 1. h (inclure D2d1. h)</dt> </dl> |
| Bibliothèque<br/> | <dl> <dt>D2d1. lib</dt> </dl>                   |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl>                   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

[Vue d’ensemble des couches](direct2d-layers-overview.md)
</dt> </dl>

�

�
