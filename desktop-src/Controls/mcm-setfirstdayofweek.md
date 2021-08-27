---
title: Message MCM_SETFIRSTDAYOFWEEK (commctrl. h)
description: Définit le premier jour de la semaine pour un contrôle de calendrier mensuel. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro calendrier monthcal SetFirstDayOfWeek.
ms.assetid: 6e0dc906-a41e-4c3a-9528-1f5428dceb8d
keywords:
- MCM_SETFIRSTDAYOFWEEK les contrôles de Windows de message
topic_type:
- apiref
api_name:
- MCM_SETFIRSTDAYOFWEEK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e34732257c18acceec3fd7db9807753e9a930e106198b33a0dd61dc27a33eef
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120077109"
---
# <a name="mcm_setfirstdayofweek-message"></a>\_Message SETFIRSTDAYOFWEEK MCM

Définit le premier jour de la semaine pour un contrôle de calendrier mensuel. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**calendrier monthcal \_ SetFirstDayOfWeek**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setfirstdayofweek) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>

Valeur de type **int** représentant le jour à définir comme premier jour de la semaine, où 0 est lundi, 1 est mardi, et ainsi de suite.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **DWORD** qui contient deux valeurs. Le mot de poids fort est une valeur **bool** différente de zéro si le premier jour de la semaine précédent n’est pas égal aux paramètres régionaux \_ IFIRSTDAYOFWEEK, ou zéro dans le cas contraire. Le mot de poids faible est une valeur INT qui représente le premier jour de la semaine précédent.

## <a name="remarks"></a>Remarques

Si le premier jour de la semaine est défini sur une valeur autre que la valeur par défaut (paramètres régionaux \_ IFIRSTDAYOFWEEK), le contrôle ne met pas automatiquement à jour les modifications de premier jour de la semaine en fonction des modifications de paramètres régionaux.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





