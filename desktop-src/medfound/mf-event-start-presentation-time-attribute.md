---
description: Heure de début de la présentation, en unités de 100 nanosecondes, mesurée en fonction de l’horloge de la présentation.
ms.assetid: d19d851c-ab4a-4a9d-bcc4-8dd4e993fa2c
title: Attribut MF_EVENT_START_PRESENTATION_TIME (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd623677de67d2101f4b1cbb3e17ce429f37f0788d99f802be0889a35dd3471e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119104825"
---
# <a name="mf_event_start_presentation_time-attribute"></a>\_Attribut heure de la \_ Présentation démarrer l’événement MF \_ \_

Heure de début de la présentation, en unités de 100 nanosecondes, mesurée en fonction de l’horloge de la présentation.

## <a name="data-type"></a>Type de données

**UINT64**

Traiter en tant que valeur **LongLong** .

## <a name="remarks"></a>Remarques

Cet attribut est utilisé avec l’événement [MESessionNotifyPresentationTime](mesessionnotifypresentationtime.md) .

Cet attribut est une valeur signée, bien qu’il soit stocké en tant que **UINT64**.

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

[**IMFAttributes::GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[**IMFAttributes::SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> </dl>

 

 




