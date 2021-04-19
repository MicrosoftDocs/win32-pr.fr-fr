---
description: Signale qu’une source de média a commencé à mettre des données en mémoire tampon.
ms.assetid: 8637dfcd-2e0c-4cf4-a216-4089c201bfc6
title: Événement MEBufferingStarted (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8eb3baf8e66d44eb67ee4c1bbc54ae2e197db081
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518577"
---
# <a name="mebufferingstarted-event"></a>Événement MEBufferingStarted

Signale qu’une source de média a commencé à mettre des données en mémoire tampon.

Une source de média peut envoyer cet événement si la source met en mémoire tampon des données pendant que la session multimédia est en cours d’exécution. Lorsque la session multimédia reçoit cet événement, elle interrompt l’horloge de la présentation jusqu’à ce que la source du média envoie l’événement [MEBufferingStopped](mebufferingstopped.md) . La session multimédia transmet également l’événement MEBufferingStarted à l’application.

Les flux d’octets qui implémentent l’interface [**IMFByteStreamBuffering**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreambuffering) envoient également cet événement.

## <a name="event-values"></a>Valeurs d’événement

Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.



| VARTYPE              | Description                           |
|----------------------|---------------------------------------|
| VT \_ vide<br/> | Aucune donnée d'événement.<br/> <br/> |



## <a name="remarks"></a>Notes

Si une source de média envoie l’événement MEBufferingStarted, elle doit envoyer l’événement [MEBufferingStopped](mebufferingstopped.md) lorsqu’elle arrête la mise en mémoire tampon des données. La source du média doit envoyer un événement MEBufferingStopped correspondant pour chaque événement MEBufferingStarted. La source du média ne doit pas transférer ces événements avant l’appel de la méthode [**IMFMediaSource :: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) de la source, ou après l’appel de la méthode [**IMFMediaSource :: Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-stop) de la source.

Si vous diffusez en continu à partir de la source réseau Media Foundation, vous pouvez obtenir la progression de la mise en mémoire tampon en interrogeant les statistiques **MFNETSOURCE \_ BUFFERPROGRESS \_ ID** . Pour plus d’informations, consultez [**MFNETSOURCE \_ Statistics \_ IDS**](/windows/desktop/api/mfidl/ne-mfidl-mfnetsource_statistics_ids).

## <a name="examples"></a>Exemples


```C++
HRESULT GetBufferProgress(IMFMediaSession *pSession, DWORD *pProgress)
{
    IPropertyStore *pProp = NULL;
    PROPVARIANT var;

    // Get the property store from the media session.
    HRESULT hr = MFGetService(
        pSession, 
        MFNETSOURCE_STATISTICS_SERVICE, 
        IID_PPV_ARGS(&pProp)
        );

    if (SUCCEEDED(hr))
    {
        PROPERTYKEY key;
        key.fmtid = MFNETSOURCE_STATISTICS;
        key.pid = MFNETSOURCE_BUFFERPROGRESS_ID;

        hr = pProp->GetValue(key, &var);
    }

    if (SUCCEEDED(hr))
    {
        *pProgress = var.lVal;
    }

    PropVariantClear(&var);
    SafeRelease(&pProp);
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
</dt> <dt>

[Mise en réseau dans Media Foundation](networking-in-media-foundation.md)
</dt> </dl>

 

 




