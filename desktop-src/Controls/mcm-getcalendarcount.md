---
title: Message MCM_GETCALENDARCOUNT (commctrl. h)
description: Obtient le nombre de calendriers actuellement affichés dans le contrôle calendrier. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro calendrier monthcal GetCalendarCount.
ms.assetid: b9463f02-d37b-49b0-8387-0938020c23ee
keywords:
- MCM_GETCALENDARCOUNT les contrôles de Windows de message
topic_type:
- apiref
api_name:
- MCM_GETCALENDARCOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9379aa8c273451ba53c2a13d6190712212765b46dc1052a08b6d03ae4ae32e61
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019047"
---
# <a name="mcm_getcalendarcount-message"></a>\_Message GETCALENDARCOUNT MCM

Obtient le nombre de calendriers actuellement affichés dans le contrôle calendrier. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**calendrier monthcal \_ GetCalendarCount**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getcalendarcount) .

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

Nombre de calendriers actuellement affichés dans le contrôle calendrier. Le nombre maximal de calendriers autorisés est 12.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





