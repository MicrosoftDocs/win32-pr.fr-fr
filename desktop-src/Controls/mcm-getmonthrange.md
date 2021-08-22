---
title: Message MCM_GETMONTHRANGE (commctrl. h)
description: Récupère des informations de date (à l’aide de structures SYSTEMTIME) qui représentent les limites haute et basse de l’affichage d’un contrôle Month Calendar. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro calendrier monthcal GetMonthRange.
ms.assetid: f50ac4b7-1f58-4639-8c78-341bb33db3c3
keywords:
- MCM_GETMONTHRANGE les contrôles de Windows de message
topic_type:
- apiref
api_name:
- MCM_GETMONTHRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc55f9732199f2e6e031248003c6dcad4abe8cb713182081666cfbee6a4ce50b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119319579"
---
# <a name="mcm_getmonthrange-message"></a>\_Message GETMONTHRANGE MCM

Récupère des informations de date (à l’aide de structures [**SystemTime**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) ) qui représentent les limites haute et basse de l’affichage d’un contrôle Month Calendar. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**calendrier monthcal \_ GetMonthRange**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getmonthrange) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Valeur spécifiant l’étendue des limites de plage à récupérer. Cette valeur doit être l’une des suivantes :



| Valeur                                                                                                                                                      | Signification                                                                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| <span id="GMR_DAYSTATE"></span><span id="gmr_daystate"></span><dl> <dt>**GMR \_ DAYSTATE**</dt> </dl> | Inclut les mois précédents et de fin de la plage visible qui ne sont affichés que partiellement. <br/> |
| <span id="GMR_VISIBLE"></span><span id="gmr_visible"></span><dl> <dt>**GMR \_ visible**</dt> </dl>    | Inclut uniquement les mois qui sont entièrement affichés. <br/>                                    |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers un tableau à deux éléments de structures [**SystemTime**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) qui recevra les limites inférieure et supérieure de la portée spécifiée par *wParam*. Les limites inférieure et supérieure sont placées dans *lprgSysTimeArray* \[ 0 \] et *lprgSysTimeArray* \[ 1 \] , respectivement. Ce paramètre doit être une adresse valide et ne peut pas avoir la **valeur null**.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur INT qui représente la plage, en mois, fractionnée par les deux limites retournées à *lParam*.

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

 

