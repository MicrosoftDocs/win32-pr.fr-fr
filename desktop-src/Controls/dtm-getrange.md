---
title: Message DTM_GETRANGE (commctrl. h)
description: Obtient l’heure système actuelle minimale et maximale autorisée pour un contrôle de sélecteur de dates et d’heures (PAO). Vous pouvez envoyer ce message de manière explicite ou utiliser la \_ macro DateTime GetRange.
ms.assetid: 190cada6-49ee-483f-a464-d3d789127159
keywords:
- DTM_GETRANGE les contrôles de Windows de message
topic_type:
- apiref
api_name:
- DTM_GETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a50a2ae9fe4ca77198f9e63548f709e0f571fdb0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127239358"
---
# <a name="dtm_getrange-message"></a>\_Message DTM GETRANGE

Obtient l’heure système actuelle minimale et maximale autorisée pour un contrôle de sélecteur de dates et d’heures (PAO). Vous pouvez envoyer ce message de manière explicite ou utiliser la macro [**DateTime \_ GetRange**](/windows/desktop/api/Commctrl/nf-commctrl-datetime_getrange) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers un tableau à deux éléments de structures [**SystemTime**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) .

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne une valeur **DWORD** qui est une combinaison de GDTR \_ min ou GDTR \_ Max. Le premier élément du tableau [**SystemTime**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) contient l’heure minimale autorisée si GDTR \_ min est défini. Le deuxième élément du tableau **SystemTime** contient le temps maximal autorisé si GDTR \_ Max est défini.

## <a name="remarks"></a>Remarques

Le sélecteur de date et d’heure affiche uniquement les dates/heures qui se trouvent dans la plage spécifiée, ce qui empêche l’utilisateur de sélectionner une date et une heure situées en dehors de la plage. Si le message [**DTM \_ SETSYSTEMTIME**](dtm-setsystemtime.md) spécifie une date et une heure qui se situent en dehors de la plage, l’opération échoue.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

