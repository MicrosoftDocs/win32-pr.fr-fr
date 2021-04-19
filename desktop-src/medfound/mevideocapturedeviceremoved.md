---
description: Envoyé par le IMFMediaSource qui encapsule l’appareil pour indiquer que l’appareil a été supprimé.
ms.assetid: 107AFF19-B444-4B62-9217-46A99AC3632C
title: Événement MEVideoCaptureDeviceRemoved (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e3276f53f86bdce78825b94828577eab9e40954
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106529321"
---
# <a name="mevideocapturedeviceremoved-event"></a>Événement MEVideoCaptureDeviceRemoved

Envoyé par le [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) qui encapsule l’appareil pour indiquer que l’appareil a été supprimé.

## <a name="event-values"></a>Valeurs d’événement

Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.



| VARTYPE               | Description                           |
|-----------------------|---------------------------------------|
| VT \_ vide <br/> | Aucune donnée d'événement.<br/> <br/> |



## <a name="remarks"></a>Notes

Cet événement est envoyé par le [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) qui encapsule l’appareil.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 8 uniquement\]<br/>                                                               |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Mfobjects. h (inclure Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Événements de Media Foundation](media-foundation-events.md)
</dt> </dl>

 

 




