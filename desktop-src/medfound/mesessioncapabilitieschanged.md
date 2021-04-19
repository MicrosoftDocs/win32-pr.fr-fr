---
description: Déclenché par la session multimédia lorsque les fonctionnalités de session changent.
ms.assetid: d59fd3a0-29db-434c-b6ba-d9beb33bd965
title: Événement MESessionCapabilitiesChanged (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0612b705571c50a6adcbde4afe93b42a524a950
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524963"
---
# <a name="mesessioncapabilitieschanged-event"></a>Événement MESessionCapabilitiesChanged

Déclenché par la session multimédia lorsque les fonctionnalités de session changent.

## <a name="event-values"></a>Valeurs d’événement

Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.



| VARTYPE              | Description                           |
|----------------------|---------------------------------------|
| VT \_ vide<br/> | Aucune donnée d'événement.<br/> <br/> |



## <a name="remarks"></a>Notes

L’événement contient les attributs suivants.



| Attribut                                                                     | Description                                      |
|-------------------------------------------------------------------------------|--------------------------------------------------|
| [**\_SESSIONCAPS d’événements MF \_**](mf-event-sessioncaps-attribute.md)              | Nouveaux indicateurs de fonctionnalités de session.                  |
| [**\_ \_ SESSIONCAPS Delta d’événement MF \_**](mf-event-sessioncaps-delta-attribute.md) | Indique les indicateurs de fonctionnalités qui ont été modifiés. |



 

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

 

 




