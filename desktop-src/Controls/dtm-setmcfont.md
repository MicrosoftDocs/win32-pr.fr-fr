---
title: Message DTM_SETMCFONT (commctrl. h)
description: Définit la police utilisée par le contrôle de calendrier mensuel enfant du contrôle de la date et de l’heure (PAO). Vous pouvez envoyer ce message de manière explicite ou utiliser la \_ macro DateTime SetMonthCalFont.
ms.assetid: 5033e975-9b68-438a-99c3-80ca02cd59e7
keywords:
- DTM_SETMCFONT les contrôles de message Windows
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
ms.openlocfilehash: b148ffb95acd82257265bf0bab53000b10803793
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466118"
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
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





