---
description: MEDeviceStreamCreated est un type d’événement multimédia étendu généré avec un événement de média MEUnknown par la MFT de l’appareil.
ms.assetid: 8aaa6908-0f2e-4a73-9362-69f42b74f495
title: Événement MEDeviceStreamCreated (mftransform. h)
ms.topic: article
ms.date: 08/31/2018
ms.openlocfilehash: 99e13dae5db9d680909a435d5520f6b07d7d4b6c11782c340b72fcdd0eddc53a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117878066"
---
# <a name="medevicestreamcreated-event"></a>Événement MEDeviceStreamCreated

MEDeviceStreamCreated est un type d’événement multimédia étendu généré avec un événement de média MEUnknown par la MFT de l’appareil.

Ce type d’événement multimédia étendu n’a pas de charge utile.  Le HRESULT approprié doit être fourni par le biais de la méthode [**IMFMediaEvent :: GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus) .




## <a name="remarks"></a>Remarques

Cet événement de média étendu doit être envoyé par la MFT de l’appareil dans le cadre de la sélection du type de média sur le flux de sortie de l’DMFT.  Lorsque le SetOutputStreamState est appelé sur l’interface IMFDeviceTransform, le DMFT est chargé de signaler la modification dans les États de flux d’entrée requis avec l’événement de média [METransformInputStreamStateChanged](/windows-hardware/drivers/stream/metransforminputstreamstatechanged) . Lorsque la modification de l’état du flux d’entrée a été reconnue par le pipeline avec l’appel de SetInputStreamState du DMFT, le DMFT est chargé d’effectuer sa configuration d’état interne et de déclencher le type d’événement multimédia étendu **MEDeviceStreamCreated** .

Si ce type d’événement multimédia étendu n’est pas déclenché, Device Transform Manager ne remet pas d’images d’entrée au DMFT.
Le type d’événement de média étendu doit également être défini en tant qu’attribut de IMFMediaEvent, l’ID de flux de sortie à l’aide de l’attribut **MF_EVENT_MFT_INPUT_STREAM_ID** .

```cpp
IMFMediaEvent* pMediaEvent = nullptr;

hr = MFCreateMediaEvent (MEUnknown,
                         MEDeviceStreamCreated,
                         S_OK,
                         nullptr,
                         &pMediaEvent);
if (SUCCEEDED(hr))
{
    hr = pMediaEvent->SetUINT32(MF_EVENT_MFT_INPUT_STREAM_ID, GetOutputStreamId());
}

if (SUCCEEDED(hr))
{
    hr = m_pEventQueue->QueueEvent(pMediaEvent);
}

if (nullptr != pMediaEvent)
{
    pMediaEvent->Release();
    pMediaEvent = nullptr;
}

return hr;
```

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10 \[ applications de bureau uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Windows Server 2016 \[ applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>mftransform. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Événements de Media Foundation](media-foundation-events.md)
</dt> <dt>

[Convertisseur audio de streaming](streaming-audio-renderer.md)
</dt> </dl>

 

 
