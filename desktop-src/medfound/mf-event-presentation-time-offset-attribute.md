---
description: Décalage entre l’heure de présentation et les horodatages de la source du média.
ms.assetid: 450f3c39-063e-4bf3-838a-0f7c240d6647
title: Attribut MF_EVENT_PRESENTATION_TIME_OFFSET (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 030d9d10eb5daf4fa1c920ad027397710b937881
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862958"
---
# <a name="mf_event_presentation_time_offset-attribute"></a>Attribut de décalage de l’heure de présentation de l' \_ événement MF \_ \_ \_

Décalage entre l’heure de présentation et les horodatages de la source du média.

## <a name="data-type"></a>Type de données

**UINT64**

## <a name="remarks"></a>Notes

Le décalage est calculé comme suit : décalage = heure de la présentation − heure source. Cet attribut est utilisé avec les événements suivants :

-   [MESessionNotifyPresentationTime](mesessionnotifypresentationtime.md)
-   [MESessionStarted](mesessionstarted.md)

La constante GUID de cet attribut est exportée à partir de mfuuid. lib.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributs d'événement](event-attributes.md)
</dt> <dt>

[**IMFAttributes::GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[**IMFAttributes::SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> </dl>

 

 




