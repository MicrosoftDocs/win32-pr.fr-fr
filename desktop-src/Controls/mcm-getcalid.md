---
title: Message MCM_GETCALID (commctrl. h)
description: Obtient l’ID de calendrier pour le contrôle de calendrier donné. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro calendrier monthcal GetCALID.
ms.assetid: ecfab4f3-a5af-445d-8b90-243b646524a6
keywords:
- MCM_GETCALID les contrôles de Windows de message
topic_type:
- apiref
api_name:
- MCM_GETCALID
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 148db880fe941c3b7df045c0ecdd4fbc9303203eace2b3be3ab38831aa4e3644
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118170186"
---
# <a name="mcm_getcalid-message"></a>\_Message GETCALID MCM

Obtient l’ID de calendrier pour le contrôle de calendrier donné. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**calendrier monthcal \_ GetCALID**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getcalid) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Doit être zéro.

</dd> <dt>

*lParam* 
</dt> <dd>

Doit être zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

ID du calendrier actuel. Une des constantes d' [identificateurs de calendrier](/windows/desktop/Intl/calendar-identifiers) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

