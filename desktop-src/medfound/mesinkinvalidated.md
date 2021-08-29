---
description: Déclenché lorsqu’un récepteur multimédia devient non valide.
ms.assetid: fa75926e-7cef-44da-9efe-f2f86fd4fd45
title: Événement MESinkInvalidated (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b002ffc47f8a47d9c7b2228a9a4d7ad7441b70aa08d12f74ece7590fe5a7088e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119941439"
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



## <a name="remarks"></a>Remarques

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
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Mfobjects. h (inclure Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Événements de Media Foundation](media-foundation-events.md)
</dt> </dl>

 

 




