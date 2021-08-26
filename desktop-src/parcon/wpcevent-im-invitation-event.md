---
description: Événement par utilisateur fourni pour l’initiation de la journalisation des conversations par les clients de messagerie instantanée.
ms.assetid: b2cd1d37-9993-4990-83b7-b147a109e4af
title: Événement WPCEVENT_IM_INVITATION (Wpcevent. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f29b1adc556e29e03f7c8a189567b98055187f80d1574e201c54e3af0c1c0aca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119951389"
---
# <a name="wpcevent_im_invitation-event"></a>\_Événement d' \_ invitation im WPCEVENT

Événement par utilisateur fourni pour l’initiation de la journalisation des conversations par les clients de messagerie instantanée.


```C++
const EVENT_DESCRIPTOR WPCEVENT_IM_INVITATION = {0x7, 0x0, 0x10, 0x4, 0x16, 0x7, 0x8000000000000030};
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

Chaîne d’identité du compte de messagerie instantanée.

</dd> <dt>

*ConvID* 
</dt> <dd>

Identificateur de la conversation.

</dd> <dt>

*RequestingIP* 
</dt> <dd>

Chaîne qui contient l’adresse IP de l’ordinateur qui envoie l’invitation.

</dd> <dt>

*Expéditeur* 
</dt> <dd>

Chaîne d’identité du compte de messagerie instantanée pour le compte qui émet l’invitation.

</dd> <dt>

*Motif* 
</dt> <dd>

Valeur de l’énumération [**WPCFLAG \_ ISBLOCKED**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) qui indique des informations sur les événements dont l’utilisation est bloquée et sur les contrôles en place.

</dd> <dt>

*RecipCount* 
</dt> <dd>

Nombre de destinataires qui reçoivent l’invitation et dont les identités sont définies dans le champ destinataire.

</dd> <dt>

*Recipient* 
</dt> <dd>

Chaîne délimitée qui contient les chaînes d’identité du compte de messagerie instantanée pour les destinataires de l’invitation.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                             |
| En-tête<br/>                   | <dl> <dt>Wpcevent. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Utilisation des API de journalisation pour les contrôles parentaux](using-logging-apis-for-parental-controls.md)
</dt> <dt>

[**WPC \_ args \_ CONVERSATIONINITEVENT**](/windows/win32/api/wpcevent/ne-wpcevent-wpc_args_conversationinitevent)
</dt> </dl>

 

 




