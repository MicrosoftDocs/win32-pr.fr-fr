---
description: Événement par utilisateur généré par une application de messagerie instantanée quand une entité tente de joindre une conversation en cours dans le contrôle parental.
ms.assetid: 5251234b-0280-4d5d-80f5-295d720a89d1
title: Événement WPCEVENT_IM_JOIN (Wpcevent. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b020eb3d4204f946002f59f472e5c95b715f88f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864769"
---
# <a name="wpcevent_im_join-event"></a>\_Événement de \_ jointure WPCEVENT im

Événement par utilisateur généré par une application de messagerie instantanée quand une entité tente de joindre une conversation en cours dans le contrôle parental.


```C++
const EVENT_DESCRIPTOR WPCEVENT_IM_JOIN = {0x8, 0x0, 0x10, 0x4, 0x16, 0x8, 0x8000000000000030};
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*AppName* 
</dt> <dd>

Nom de l’application qui génère l’événement.

</dd> <dt>

*AppVersion* 
</dt> <dd>

Chaîne de version de l’application qui génère l’événement.

</dd> <dt>

*AccountName* 
</dt> <dd>

Chaîne d’identité du compte de messagerie instantanée pour cet utilisateur.

</dd> <dt>

*ConvID* 
</dt> <dd>

Identificateur de cette conversation.

</dd> <dt>

*JoiningIP* 
</dt> <dd>

Chaîne qui contient l’adresse IP de l’ordinateur qui rejoint cette conversation.

</dd> <dt>

*JoiningUser* 
</dt> <dd>

Chaîne d’identité du compte de messagerie instantanée pour l’utilisateur qui rejoint.

</dd> <dt>

*Motif* 
</dt> <dd>

Valeur de l’énumération [**WPCFLAG \_ ISBLOCKED**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) qui indique des informations sur les événements dont l’utilisation est bloquée et sur les contrôles en place.

</dd> <dt>

*MemberCount* 
</dt> <dd>

Nombre de participants qui participent à la conversation et qui ont des identités définies dans le champ membre.

</dd> <dt>

*Membre* 
</dt> <dd>

Chaîne délimitée qui contient les chaînes d’identité du compte de messagerie instantanée pour tous les membres actuels de cette conversation.

</dd> <dt>

*Expéditeur* 
</dt> <dd>

Chaîne d’identité du compte de messagerie instantanée pour l’utilisateur qui effectue la demande de jointure de la conversation.

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

 

 




