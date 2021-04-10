---
description: 'Déclenché après la fin asynchrone de la méthode IMFMediaSession :: SetTopology. La session multimédia déclenche cet événement après la résolution de la topologie en une topologie complète et la mise en file d’attente de la topologie pour la lecture.'
ms.assetid: 22a298b7-d32b-44ed-b0a1-4e0398ecfe04
title: Événement MESessionTopologySet (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 338668b0ec9b4dd81140edfb55a823a5a595459b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951548"
---
# <a name="mesessiontopologyset-event"></a>Événement MESessionTopologySet

Déclenché après la fin asynchrone de la méthode [**IMFMediaSession :: SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) . La session multimédia déclenche cet événement après la résolution de la topologie en une topologie complète et la mise en file d’attente de la topologie pour la lecture.

## <a name="event-values"></a>Valeurs d’événement

Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.



| VARTYPE                | Description                                                                                              |
|------------------------|----------------------------------------------------------------------------------------------------------|
| VT \_ vide<br/>   | Aucune donnée d'événement.<br/> <br/>                                                                    |
| VT \_ inconnu<br/> | Pointeur vers l’interface [**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) de la topologie complète.<br/> <br/> |



## <a name="examples"></a>Exemples

L’exemple suivant récupère le pointeur [**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) à partir d’un événement MESessionTopologySet.


```
HRESULT GetTopologyFromEvent(IMFMediaEvent *pEvent, IMFTopology **ppTopology)
{
    HRESULT hr = S_OK;
    PROPVARIANT var;

    PropVariantInit(&var);
    hr = pEvent->GetValue(&var);
    if (SUCCEEDED(hr))
    {
        if (var.vt != VT_UNKNOWN)
        {
            hr = E_UNEXPECTED;
        }
    }
    if (SUCCEEDED(hr))
    {
        hr = var.punkVal->QueryInterface(__uuidof(IMFTopology), (void**)ppTopology);
    }
    PropVariantClear(&var);
    return hr;
}
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Mfobjects. h (inclure Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Événements de Media Foundation](media-foundation-events.md)
</dt> </dl>

 

 




