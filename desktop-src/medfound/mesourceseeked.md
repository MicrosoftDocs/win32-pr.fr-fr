---
description: 'Déclenché quand une source multimédia cherche à une nouvelle position. Une source de média déclenche cet événement si la source est en cours d’exécution ou en pause et que l’application appelle IMFMediaSource :: Start avec une heure de début qui n’est pas égale à la position actuelle.'
ms.assetid: 51ce770e-ddc7-41c1-8e31-59481cafe2b0
title: Événement MESourceSeeked (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 589e6619b4b4147da65a327681ad4ed2eace89c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524481"
---
# <a name="mesourceseeked-event"></a>Événement MESourceSeeked

Déclenché quand une source multimédia cherche à une nouvelle position. Une source de média déclenche cet événement si la source est en cours d’exécution ou en pause et que l’application appelle [**IMFMediaSource :: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) avec une heure de début qui n’est pas égale à la position actuelle.

## <a name="event-values"></a>Valeurs d’événement

Les valeurs possibles récupérées à partir de [**IMFMediaEvent :: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) sont les suivantes.



| VARTYPE           | Description                                                                |
|-------------------|----------------------------------------------------------------------------|
| Le \_ i8 VT<br/> | Nouvelle position de départ, en unités de 100 nanosecondes.<br/> <br/> |



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

 

 




