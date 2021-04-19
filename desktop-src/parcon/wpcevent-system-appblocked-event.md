---
description: Événement au niveau système généré par les stratégies de restriction logicielle (SRP) lorsqu’une application est bloquée par des règles plus sûres.
ms.assetid: 6772a2c9-35c1-4b75-94e4-baa84af7c0ed
title: Événement WPCEVENT_SYSTEM_APPBLOCKED (Wpcevent. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67c3f6255911f59717c1fa594aee4bfc49f6c5a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519088"
---
# <a name="wpcevent_system_appblocked-event"></a>\_ \_ Événement APPBLOCKED système WPCEVENT

Événement au niveau système généré par les stratégies de restriction logicielle (SRP) lorsqu’une application est bloquée par des règles plus sûres.


```C++
const EVENT_DESCRIPTOR WPCEVENT_SYSTEM_APPBLOCKED = {0x10, 0x0, 0x10, 0x4, 0x16, 0x10, 0x8000000000000010};
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Confirmé* 
</dt> <dd>

Heure à laquelle le bloc s’est produit.

</dd> <dt>

*l'UserId* 
</dt> <dd>

Identificateur de sécurité de l’utilisateur qui tente de lancer l’application.

</dd> <dt>

*Chemin d’accès* 
</dt> <dd>

Chemin d’accès à l’application que l’utilisateur tente de lancer.

</dd> <dt>

*RuleID* 
</dt> <dd>

ID de la règle dans le jeu de règles de sécurité de contrôle parental qui bloquent l’exécution.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                             |
| En-tête<br/>                   | <dl> <dt>Wpcevent. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Utilisation des API de journalisation pour les contrôles parentaux](using-logging-apis-for-parental-controls.md)
</dt> <dt>

[**WPC \_ args \_ CONVERSATIONINITEVENT**](/windows/win32/api/wpcevent/ne-wpcevent-wpc_args_conversationinitevent)
</dt> </dl>

 

 




