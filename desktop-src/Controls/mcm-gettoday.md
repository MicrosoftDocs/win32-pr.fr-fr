---
title: Message MCM_GETTODAY (commctrl. h)
description: Récupère les informations de date pour la date spécifiée sous la forme \ 0034 ; Today \ 0034 ; pour un contrôle Month Calendar. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro calendrier monthcal GetToday.
ms.assetid: a79feb57-6aa3-4c96-95f3-7018b6b8327f
keywords:
- MCM_GETTODAY les contrôles de message Windows
topic_type:
- apiref
api_name:
- MCM_GETTODAY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21538af3c573b3d972b7f16bfe024e0d36211644
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942199"
---
# <a name="mcm_gettoday-message"></a>\_Message GETTODAY MCM

Récupère les informations de date pour la date spécifiée comme « Today » pour un contrôle Month Calendar. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**calendrier monthcal \_ GetToday**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_gettoday) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**SystemTime**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) qui recevra les informations de date. Ce paramètre doit être une adresse valide et ne peut pas avoir la **valeur null**.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur différente de zéro en cas de réussite, ou zéro dans le cas contraire.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Heures dans le contrôle Month Calendar](month-calendar-controls.md)
</dt> </dl>

 

