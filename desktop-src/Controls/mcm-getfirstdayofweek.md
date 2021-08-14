---
title: Message MCM_GETFIRSTDAYOFWEEK (commctrl. h)
description: Récupère le premier jour de la semaine pour un contrôle de calendrier mensuel. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro calendrier monthcal GetFirstDayOfWeek.
ms.assetid: bbbc1c45-5693-4a79-908a-ec6e8ef8b218
keywords:
- MCM_GETFIRSTDAYOFWEEK les contrôles de Windows de message
topic_type:
- apiref
api_name:
- MCM_GETFIRSTDAYOFWEEK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1bc0ddcd36da0b993f3a05092c878319a6749d9eb5a3043ce910eba1462beef9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119319649"
---
# <a name="mcm_getfirstdayofweek-message"></a>\_Message GETFIRSTDAYOFWEEK MCM

Récupère le premier jour de la semaine pour un contrôle de calendrier mensuel. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**calendrier monthcal \_ GetFirstDayOfWeek**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getfirstdayofweek) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **DWORD** qui contient deux valeurs. Le mot de poids fort est une valeur **bool** différente de zéro si le premier jour de la semaine est défini sur une valeur autre que locale \_ IFIRSTDAYOFWEEK, ou sur zéro dans le cas contraire. Le mot de poids faible est une valeur INT qui représente le premier jour de la semaine, où 0 est lundi, 1 est mardi, et ainsi de suite.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





