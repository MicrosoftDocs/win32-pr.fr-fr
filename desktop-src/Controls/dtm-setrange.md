---
title: Message DTM_SETRANGE (commctrl. h)
description: Définit les heures système minimale et maximale autorisées pour un contrôle de sélecteur de dates et d’heures (PAO). Vous pouvez envoyer ce message explicitement ou utiliser la \_ macro DateTime SetRange.
ms.assetid: ef0f48f2-906e-4ae0-839d-177e0fb7f14e
keywords:
- DTM_SETRANGE les contrôles de Windows de message
topic_type:
- apiref
api_name:
- DTM_SETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 380bd35bd590facd1368507f2bf5900c05c4f68557cf1e4201058dfbacdb282d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119877729"
---
# <a name="dtm_setrange-message"></a>\_Message DTM SEtrange

Définit les heures système minimale et maximale autorisées pour un contrôle de sélecteur de dates et d’heures (PAO). Vous pouvez envoyer ce message explicitement ou utiliser la macro [**DateTime \_ SetRange**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_setrange) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Valeur qui spécifie les valeurs de plage valides. Ce paramètre peut être une combinaison des valeurs suivantes :



| Valeur                                                                                                                                          | Signification                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GDTR_MIN"></span><span id="gdtr_min"></span><dl> <dt>**GDTR \_ min.**</dt> </dl> | Le premier élément du tableau de la structure [**SystemTime**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) est valide et sera utilisé pour définir l’heure minimale autorisée du système.<br/>  |
| <span id="GDTR_MAX"></span><span id="gdtr_max"></span><dl> <dt>**GDTR \_ Max**</dt> </dl> | Le deuxième élément du tableau de la structure [**SystemTime**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) est valide et sera utilisé pour définir l’heure maximale autorisée du système.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers un tableau à deux éléments de structures [**SystemTime**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) . Le premier élément du tableau **SystemTime** contient l’heure minimale autorisée. Le deuxième élément du tableau **SystemTime** contient le temps maximum autorisé. Il n’est pas nécessaire de remplir un élément de tableau qui n’est pas spécifié dans le paramètre *wParam* .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur différente de zéro en cas de réussite, ou zéro dans le cas contraire.

## <a name="remarks"></a>Remarques

Le sélecteur de date et d’heure affiche uniquement les dates/heures qui se trouvent dans la plage spécifiée, ce qui empêche l’utilisateur de sélectionner une date et une heure situées en dehors de la plage. Si le message [**DTM \_ SETSYSTEMTIME**](dtm-setsystemtime.md) spécifie une date et une heure qui se situent en dehors de la plage, l’opération échoue.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

