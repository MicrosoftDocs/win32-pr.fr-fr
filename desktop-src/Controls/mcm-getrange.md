---
title: Message MCM_GETRANGE (commctrl. h)
description: Récupère les dates minimales et maximales autorisées définies pour un contrôle Month Calendar. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro calendrier monthcal GetRange.
ms.assetid: 5000053a-2975-4781-b3c9-83f9763f679a
keywords:
- MCM_GETRANGE les contrôles de Windows de message
topic_type:
- apiref
api_name:
- MCM_GETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26f8b9d5a485b12caf720afe518a2fc5499e55eba07c90c2fde1bb34eea2404b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117830393"
---
# <a name="mcm_getrange-message"></a>\_Message GETRANGE MCM

Récupère les dates minimales et maximales autorisées définies pour un contrôle Month Calendar. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**calendrier monthcal \_ GetRange**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getrange) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers un tableau à deux éléments de structures [**SystemTime**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) qui recevra les informations de limite de date. La limite minimale est définie dans *lprgSysTimeArray* \[ 0 \] et *lprgSysTimeArray* \[ 1 \] reçoit la limite maximale. Si l’un des éléments a la valeur tous les zéros, aucune limite correspondante n’est définie pour le contrôle Month Calendar. Ce paramètre doit être une adresse valide et ne peut pas avoir la **valeur null**.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une **valeur DWORD** qui peut être égale à zéro (aucune limite n’est définie) ou une combinaison des valeurs suivantes qui spécifient des informations de limite :



| Code de retour                                                                              | Description                                                                                                                        |
|------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GDTR \_ Max**</dt> </dl> | Une limite maximale est définie pour le contrôle ; *lprgSysTimeArray* \[ 0 \] est valide et contient les informations de date applicables. <br/> |
| <dl> <dt>**GDTR \_ min.**</dt> </dl> | Une limite minimale est définie pour le contrôle ; *lprgSysTimeArray* \[ 1 \] est valide et contient les informations de date applicables. <br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Heures dans le contrôle Month Calendar](month-calendar-controls.md)
</dt> </dl>

 

