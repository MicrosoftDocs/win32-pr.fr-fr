---
description: Déclenché lorsqu’un récepteur multimédia devient non valide.
ms.assetid: fa75926e-7cef-44da-9efe-f2f86fd4fd45
title: Événement MESinkInvalidated (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46807a45e907999b34190f9678bd3dc0051680ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201616"
---
# <a name="mesinkinvalidated-event"></a>Événement MESinkInvalidated

Déclenché lorsqu’un récepteur multimédia devient non valide.

## <a name="event-values"></a>Valeurs d’événement

Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.



| VARTYPE              | Description                           |
|----------------------|---------------------------------------|
| VT \_ vide<br/> | Aucune donnée d'événement.<br/> <br/> |



## <a name="attributes"></a>Attributs

Les attributs suivants sont définis pour cet événement.



| Attribut                                                                    | Description                                                              |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| [**\_ \_ nœud sortie de l’événement MF \_**](mf-event-output-node-attribute.md)<br/> | Identifie le nœud de topologie de ce récepteur multimédia.<br/> <br/> |



## <a name="remarks"></a>Notes

La session multimédia déclenche cet événement si elle reçoit l’un des événements suivants du récepteur multimédia :

-   [MEAudioSessionDeviceRemoved](meaudiosessiondeviceremoved.md)

-   [MEAudioSessionDisconnected](meaudiosessiondisconnected.md)

-   [MEAudioSessionExclusiveModeOverride](meaudiosessionexclusivemodeoverride.md)

-   [MEAudioSessionFormatChanged](meaudiosessionformatchanged.md)

-   [MEAudioSessionServerShutdown](meaudiosessionservershutdown.md)

Un récepteur multimédia peut également déclencher cet événement, auquel cas la session multimédia définit l’attribut [**de \_ \_ \_ nœud sortie d’événement MF**](mf-event-output-node-attribute.md) sur l’événement et transfère l’événement à l’application.

Si l’application reçoit cet événement, elle a besoin de recréer le récepteur multimédia et de recréer la file d’attente de la topologie.

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

 

 




