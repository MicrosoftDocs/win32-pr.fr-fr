---
title: Message IPM_SETRANGE (commctrl. h)
description: Définit la plage valide pour le champ spécifié dans le contrôle d’adresse IP.
ms.assetid: 03068c5d-822f-459d-8f79-e7f0430a27bf
keywords:
- IPM_SETRANGE les contrôles de Windows de message
topic_type:
- apiref
api_name:
- IPM_SETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d599619fa9a065a27a9721b890f6d52c496bf646504009e1950b7ca1279f8a2c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119434469"
---
# <a name="ipm_setrange-message"></a>\_Message IPM SEtrange

Définit la plage valide pour le champ spécifié dans le contrôle d’adresse IP.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Index de champ de base zéro auquel la plage sera appliquée.

</dd> <dt>

*lParam* 
</dt> <dd>

Valeur de **mot** qui contient la limite inférieure de la plage dans l’octet de poids faible et la limite supérieure dans l’octet de poids fort. Ces deux valeurs sont inclusives. La macro [**MAKEIPRANGE**](/windows/desktop/api/Commctrl/nf-commctrl-makeiprange) peut également être utilisée pour créer la plage.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur différente de zéro en cas de réussite, ou zéro dans le cas contraire.

## <a name="remarks"></a>Remarques

Si l’utilisateur entre une valeur dans le champ qui est en dehors de cette plage, le contrôle envoie la notification [IPN \_ FIELDCHANGED](ipn-fieldchanged.md) avec la valeur entrée. Si la valeur est toujours en dehors de la plage après l’envoi de la notification, le contrôle tente de modifier la valeur entrée à la limite de plage la plus proche.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





