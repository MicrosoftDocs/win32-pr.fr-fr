---
description: Spécifie si la source de Sequencer a annulé une topologie.
ms.assetid: b7252336-1612-43fc-8f08-1fdfdbb293eb
title: Attribut MF_EVENT_SOURCE_TOPOLOGY_CANCELED (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef612c8a1081ecc26eaa9dc593a5906ff965d0387ab02490eedd68f7fbf5e813
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118060656"
---
# <a name="mf_event_source_topology_canceled-attribute"></a>Attribut d’annulation de la topologie de la \_ source d’événements MF \_ \_ \_

Spécifie si la [source de Sequencer](sequencer-source.md) a annulé une topologie.

## <a name="data-type"></a>Type de données

**UINT32**

Traiter en tant que valeur booléenne.

## <a name="remarks"></a>Remarques

Cet attribut est utilisé avec les événements suivants :

-   [MEEndOfPresentationSegment](meendofpresentationsegment.md)
-   [MEEndOfPresentation](meendofpresentation.md)

Si cet attribut est présent et différent de zéro, cela signifie que le segment de présentation s’est terminé parce que la source de Sequencer a annulé la topologie. Dans le cas contraire, le segment de présentation s’est terminé normalement.

La constante GUID de cet attribut est exportée à partir de mfuuid. lib.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributs d'événement](event-attributes.md)
</dt> <dt>

[**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[Événements de source de Sequencer](sequencer-source-events.md)
</dt> </dl>

 

 




