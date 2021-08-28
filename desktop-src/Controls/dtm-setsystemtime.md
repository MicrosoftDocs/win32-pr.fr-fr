---
title: Message DTM_SETSYSTEMTIME (commctrl. h)
description: Définit l’heure dans un contrôle de sélecteur de dates et d’heures (PAO). Vous pouvez envoyer ce message de manière explicite ou utiliser la \_ macro DateTime SetSystemtime.
ms.assetid: aab023ac-22ef-485b-be2f-2aa76dfcf57f
keywords:
- DTM_SETSYSTEMTIME les contrôles de Windows de message
topic_type:
- apiref
api_name:
- DTM_SETSYSTEMTIME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5acd0c6a09e3fc7bd9d068e27049329f3289a8ba1968ffae4592c7e07db9f2eb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120088969"
---
# <a name="dtm_setsystemtime-message"></a>\_Message DTM SETSYSTEMTIME

Définit l’heure dans un contrôle de sélecteur de dates et d’heures (PAO). Vous pouvez envoyer ce message de manière explicite ou utiliser la macro [**DateTime \_ SetSystemtime**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setsystemtime) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Valeur qui spécifie l’action qui doit être effectuée. Cette valeur doit être définie sur l’un des éléments suivants :



| Valeur                                                                                                                                             | Signification                                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GDT_VALID"></span><span id="gdt_valid"></span><dl> <dt>**GDT \_ valide**</dt> </dl> | Définissez le contrôle PAO en fonction des données de la structure vers laquelle *lParam* pointe. <br/>                                                                                                                                                                 |
| <span id="GDT_NONE"></span><span id="gdt_none"></span><dl> <dt>**GDT \_ None**</dt> </dl>    | Définissez le contrôle PAO sur « aucune date » et désactivez sa case à cocher. Lorsque cet indicateur est spécifié, *lParam* est ignoré. Cet indicateur s’applique uniquement aux contrôles de PAO définis sur le style [**DTS \_ SHOWNONE**](date-and-time-picker-control-styles.md) . <br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**SystemTime**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) contenant l’heure système utilisée pour définir le contrôle de PAO.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur différente de zéro en cas de réussite, ou zéro dans le cas contraire.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

