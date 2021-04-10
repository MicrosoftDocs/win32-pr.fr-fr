---
title: Message MCM_GETSELRANGE (commctrl. h)
description: Récupère des informations de date qui représentent les limites supérieure et inférieure de la plage de dates actuellement sélectionnée par l’utilisateur. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro calendrier monthcal GetSelRange.
ms.assetid: a0d0a0d5-a519-4495-a87a-2438c4590e4c
keywords:
- MCM_GETSELRANGE les contrôles de message Windows
topic_type:
- apiref
api_name:
- MCM_GETSELRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0d2f922b013a3eab525228bda4f5b99f33e70d8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941951"
---
# <a name="mcm_getselrange-message"></a>\_Message GETSELRANGE MCM

Récupère des informations de date qui représentent les limites supérieure et inférieure de la plage de dates actuellement sélectionnée par l’utilisateur. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**calendrier monthcal \_ GetSelRange**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getselrange) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers un tableau à deux éléments de structures [**SystemTime**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) qui recevra les limites inférieure et supérieure de la sélection de l’utilisateur. Les limites inférieure et supérieure sont placées dans *lprgSysTimeArray* \[ 0 \] et *lprgSysTimeArray* \[ 1 \] , respectivement. Ce paramètre doit être une adresse valide et ne peut pas avoir la **valeur null**.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur différente de zéro en cas de réussite, ou zéro dans le cas contraire. **MCM \_ GETSELRANGE** échouera s’il est appliqué à un contrôle Month Calendar qui n’utilise pas le style [**MCS \_ MultiSelect**](month-calendar-control-styles.md) .

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

 

