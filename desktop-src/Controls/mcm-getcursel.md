---
title: Message MCM_GETCURSEL (commctrl. h)
description: Récupère la date actuellement sélectionnée. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro calendrier monthcal GetCurSel.
ms.assetid: d4edc9ed-7c92-4ec8-bfa1-8ae597826b3f
keywords:
- MCM_GETCURSEL les contrôles de Windows de message
topic_type:
- apiref
api_name:
- MCM_GETCURSEL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7dece95c65e900119c7043c0d5eda22bf473e6c6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127012298"
---
# <a name="mcm_getcursel-message"></a>\_Message GETCURSEL MCM

Récupère la date actuellement sélectionnée. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**calendrier monthcal \_ GetCurSel**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getcursel) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**SystemTime**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) qui recevra les informations de date actuellement sélectionnées. Ce paramètre doit être une adresse valide et ne peut pas avoir la **valeur null**.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne une valeur différente de zéro en cas de réussite, ou zéro dans le cas contraire. Ce message échouera toujours lorsqu’il sera appliqué aux contrôles de calendrier mensuel définis sur le style [**MCS \_ MultiSelect**](month-calendar-control-styles.md) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Heures dans le contrôle Month Calendar](month-calendar-controls.md)
</dt> </dl>

 

