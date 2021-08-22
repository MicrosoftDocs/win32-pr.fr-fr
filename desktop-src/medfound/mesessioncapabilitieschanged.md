---
description: Déclenché par la session multimédia lorsque les fonctionnalités de session changent.
ms.assetid: d59fd3a0-29db-434c-b6ba-d9beb33bd965
title: Événement MESessionCapabilitiesChanged (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc97cb5168957f34cc029a982447c6d4775075ea6f9b9b250ce7b9fd7f1791d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119464869"
---
# <a name="mesessioncapabilitieschanged-event"></a>Événement MESessionCapabilitiesChanged

Déclenché par la session multimédia lorsque les fonctionnalités de session changent.

## <a name="event-values"></a>Valeurs d’événement

Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.



| VARTYPE              | Description                           |
|----------------------|---------------------------------------|
| VT \_ vide<br/> | Aucune donnée d'événement.<br/> <br/> |



## <a name="remarks"></a>Remarques

L’événement contient les attributs suivants.



| Attribut                                                                     | Description                                      |
|-------------------------------------------------------------------------------|--------------------------------------------------|
| [**\_SESSIONCAPS d’événements MF \_**](mf-event-sessioncaps-attribute.md)              | Nouveaux indicateurs de fonctionnalités de session.                  |
| [**\_ \_ SESSIONCAPS Delta d’événement MF \_**](mf-event-sessioncaps-delta-attribute.md) | Indique les indicateurs de fonctionnalités qui ont été modifiés. |



 

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

 

 




