---
title: Message DTM_SETMCFONT (commctrl. h)
description: Définit la police utilisée par le contrôle de calendrier mensuel enfant du contrôle de la date et de l’heure (PAO). Vous pouvez envoyer ce message de manière explicite ou utiliser la \_ macro DateTime SetMonthCalFont.
ms.assetid: 5033e975-9b68-438a-99c3-80ca02cd59e7
keywords:
- DTM_SETMCFONT les contrôles de Windows de message
topic_type:
- apiref
api_name:
- DTM_SETMCFONT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfa1b34c1a51e365868cbdae30e46cd299937d3d6fe33bad6c57d630a0b226fb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119877809"
---
# <a name="dtm_setmcfont-message"></a>\_Message DTM SETMCFONT

Définit la police utilisée par le contrôle de calendrier mensuel enfant du contrôle de la date et de l’heure (PAO). Vous pouvez envoyer ce message de manière explicite ou utiliser la macro [**DateTime \_ SetMonthCalFont**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setmonthcalfont) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Handle de la police qui sera définie.

</dd> <dt>

*lParam* 
</dt> <dd>

Spécifie si le contrôle doit être redessiné immédiatement lors de la définition de la police. Si ce paramètre a la **valeur true** , le contrôle se redessine lui-même.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour de ce message n’est pas utilisée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





