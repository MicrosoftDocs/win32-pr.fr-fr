---
description: Indique que la lecture du DVD a été arrêtée. Cet événement est envoyé lorsqu’un titre ou chapitre se termine et que le navigateur DVD ne trouve pas d’autres instructions de création de branche pour la lecture suivante. L’événement n’est pas envoyé lorsque l’application arrête la lecture.
ms.assetid: c8617307-d70e-48af-8e85-69105595aa10
title: EC_DVD_PLAYBACK_STOPPED (Dvdevcode. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_PLAYBACK_STOPPED
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 7a5f0b1b66e9d78309e33981910da467757a2b606b967cee5b78e86c4cc0049b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117820455"
---
# <a name="ec_dvd_playback_stopped"></a>\_lecture du DVD EC \_ \_ arrêtée

Indique que la lecture du DVD a été arrêtée. Cet événement est envoyé lorsqu’un titre ou chapitre se termine et que le [navigateur DVD](dvd-navigator-filter.md) ne trouve pas d’autres instructions de création de branche pour la lecture suivante. L’événement n’est pas envoyé lorsque l’application arrête la lecture.

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*
</dt> <dd>

Un membre de l’énumération [**DVD \_ PB s' \_ est arrêté**](/previous-versions/windows/desktop/api/dvdevcod/ne-dvdevcod-dvd_pb_stopped) , indiquant la raison de l’arrêt de la lecture.

</dd> <dt>

<span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*
</dt> <dd>

Zéro.

</dd> </dl>

## <a name="remarks"></a>Remarques

Cet événement est déclenché dans tous les domaines.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Dvdevcode. h (inclure DShow. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Applications DVD](dvd-applications.md)
</dt> <dt>

[Codes de notification des événements DVD](dvd-notification-codes.md)
</dt> <dt>

[Notification d’événements dans DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 




