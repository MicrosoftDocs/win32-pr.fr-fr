---
title: D1111 utilisation de la couche lorsque l’élément est suffisant
ms.assetid: 07fe3c66-15be-408b-a30b-a7f52919c058
description: Une couche est utilisée avec un masque d’opacité NULL, une opacité de 1,0 et un masque géométrique rectangulaire aligné sur un axe. L’API clip push/pop doit obtenir les mêmes résultats avec des performances supérieures.
keywords:
- D1111 utilisant une couche quand l’élément est suffisamment Direct2D
topic_type:
- apiref
api_name:
- D1111 Using Layer When Clip Is Sufficient
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: e8463cc3940b69e326f13df6be9602dd6073fec0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127114061"
---
# <a name="d1111-using-layer-when-clip-is-sufficient"></a>D1111 : utilisation de la couche lorsque l’élément est suffisant

PERF : une couche est utilisée avec un masque d’opacité **null** , une opacité de 1,0 et un masque géométrique rectangulaire aligné sur un axe. L’API clip push/pop doit obtenir les mêmes résultats avec des performances supérieures.

## <a name="placeholders"></a>Espaces réservés

<dl> <dt>

<span id="interface"></span><span id="INTERFACE"></span>*interface*
</dt> <dd>

Adresse de l’interface.

</dd> </dl> 

| &nbsp;      |    &nbsp;   |
|-------------|-------------|
| Niveau d’erreur | Information |



 

## <a name="examples"></a>Exemples

Le code suivant utilise [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) et [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) lorsque la couche contient uniquement une primitive (un rectangle) et que les champs de la structure des [**\_ \_ paramètres de couche d2d1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) sont définis sur les valeurs par défaut. Pour connaître les valeurs par défaut de la structure des **\_ \_ paramètres de couche d2d1** , consultez [**LayerParameter**](/windows/desktop/api/d2d1helper/nf-d2d1helper-layerparameters).


```C++
        ID2D1Layer *m_pLayer;

        hr = m_pRenderTarget->CreateLayer(D2D1::SizeF(100, 100), &m_pLayer);
        m_pRenderTarget->PushLayer(D2D1::LayerParameters(), m_pLayer);
        m_pRenderTarget->FillRectangle(D2D1::RectF(100, 50, 400, 160), m_pBlackBrush);
        m_pRenderTarget->PopLayer();
```



Cet exemple génère le message de débogage suivant :

``` syntax
DEBUG INFO - PERF - A layer is being used with a NULL opacity mask, 1.0 opacity, 
            and an axis aligned rectangular geometric mask.  
            The Push/Pop Clip API should achieve the same results with higher performance.
```

## <a name="possible-causes"></a>Causes possibles

Une couche a été utilisée lorsque les méthodes [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) et [**PopAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-popaxisalignedclip) seraient suffisantes.

 

 