---
description: Événement par utilisateur qui prend en charge jusqu’à trois champs.
ms.assetid: e6cf8008-b896-453b-9946-a6b3d94a991a
title: Événement WPCEVENT_CUSTOM (Wpcevent. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d20cb2450cd18bb0c77993622d226cfc06dff6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202707"
---
# <a name="wpcevent_custom-event"></a>\_Événement personnalisé WPCEVENT

Événement par utilisateur qui prend en charge jusqu’à trois champs.

Les événements sont affichés dans l' **Observateur d’activité** dans l' **autre** section avec la hiérarchie suivante :

1.  Publisher

2.  Application

3.  Événement


```C++
const EVENT_DESCRIPTOR WPCEVENT_CUSTOM = {0xd, 0x0, 0x10, 0x4, 0x17, 0xd, 0x8000000000000030};
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Publisher* 
</dt> <dd>

Éditeur de l’événement (par exemple, un nom de société).

</dd> <dt>

*AppName* 
</dt> <dd>

Nom de l’application qui génère l’événement.

</dd> <dt>

*AppVersion* 
</dt> <dd>

Version de l’application qui génère l’événement.

</dd> <dt>

*Event* 
</dt> <dd>

Nom de l’événement.

</dd> <dt>

*Value* 
</dt> <dd>

Champ personnalisé 1.

</dd> <dt>

*Value2* 
</dt> <dd>

Champ personnalisé 2.

</dd> <dt>

*Valeur3* 
</dt> <dd>

Champ personnalisé 3.

</dd> <dt>

*Bloqué* 
</dt> <dd>

Valeur de l’énumération [**WPCFLAG \_ ISBLOCKED**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) qui indique des informations sur les événements dont l’utilisation est bloquée et sur les contrôles en place.

</dd> <dt>

*Motif* 
</dt> <dd>

Chaîne personnalisée qui fournit des informations supplémentaires sur la raison du blocage ou non du blocage.

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

 

 




