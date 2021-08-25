---
title: Message DTM_GETMCFONT (commctrl. h)
description: Obtient la police actuellement utilisée par le contrôle de calendrier mensuel enfant du contrôle de la date et de l’heure (PAO). Vous pouvez envoyer ce message de manière explicite ou utiliser la \_ macro DateTime GetMonthCalFont.
ms.assetid: 6687a1dc-6f6d-4684-80b2-f726b08d2f3a
keywords:
- DTM_GETMCFONT les contrôles de Windows de message
topic_type:
- apiref
api_name:
- DTM_GETMCFONT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2bf60f226e7fe5d309324bc517a7fd215abe4591fd5141ff149b14e162ac9be
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119878129"
---
# <a name="dtm_getmcfont-message"></a>\_Message DTM GETMCFONT

Obtient la police actuellement utilisée par le contrôle de calendrier mensuel enfant du contrôle de la date et de l’heure (PAO). Vous pouvez envoyer ce message de manière explicite ou utiliser la macro [**DateTime \_ GetMonthCalFont**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getmonthcalfont) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur HFONT qui est le handle de la police actuelle.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





