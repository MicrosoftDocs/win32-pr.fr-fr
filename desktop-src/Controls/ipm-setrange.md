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
ms.openlocfilehash: e70df7b2b8f76f514d9a0cc6101aba2ee7cf4ec6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126999882"
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

## <a name="return-value"></a>Valeur de retour

Retourne une valeur différente de zéro en cas de réussite, ou zéro dans le cas contraire.

## <a name="remarks"></a>Notes

Si l’utilisateur entre une valeur dans le champ qui est en dehors de cette plage, le contrôle envoie la notification [IPN \_ FIELDCHANGED](ipn-fieldchanged.md) avec la valeur entrée. Si la valeur est toujours en dehors de la plage après l’envoi de la notification, le contrôle tente de modifier la valeur entrée à la limite de plage la plus proche.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





