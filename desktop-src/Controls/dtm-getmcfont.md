---
title: Message DTM_GETMCFONT (commctrl. h)
description: Obtient la police actuellement utilisée par le contrôle de calendrier mensuel enfant du contrôle de la date et de l’heure (PAO). Vous pouvez envoyer ce message de manière explicite ou utiliser la \_ macro DateTime GetMonthCalFont.
ms.assetid: 6687a1dc-6f6d-4684-80b2-f726b08d2f3a
keywords:
- DTM_GETMCFONT les contrôles de message Windows
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
ms.openlocfilehash: d799d5dbbe5e3a4cdf7eede871f9aeac451d17a4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844141"
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
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





