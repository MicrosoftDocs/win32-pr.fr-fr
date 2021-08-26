---
description: Événement par utilisateur généré par un client de messagerie lors de la tentative de réception d’un message dans le contrôle parental.
ms.assetid: 3b8d9bac-16b0-49e9-b360-b2d6e82f1753
title: Événement WPCEVENT_EMAIL_RECEIVED (Wpcevent. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a81a51e79125403504aae2ed6e823c10044ffc35ed36ff139e8333f955338d81
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119951559"
---
# <a name="wpcevent_email_received-event"></a>\_Événement WPCEVENT E-mail \_ received

Événement par utilisateur généré par un client de messagerie lors de la tentative de réception d’un message dans le contrôle parental.


```C++
const EVENT_DESCRIPTOR WPCEVENT_EMAIL_RECEIVED = {0x4, 0x0, 0x10, 0x4, 0x16, 0x4, 0x8000000000000030};
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Expéditeur* 
</dt> <dd>

Nom du compte de messagerie de l’entité émettrice.

</dd> <dt>

*AppName* 
</dt> <dd>

Nom de l’application de messagerie qui génère l’événement.

</dd> <dt>

*AppVersion* 
</dt> <dd>

Version de l’application de messagerie qui génère l’événement.

</dd> <dt>

*Subject* 
</dt> <dd>

Ligne d’objet du message reçu.

</dd> <dt>

*Motif* 
</dt> <dd>

Valeur de l’énumération [**WPCFLAG \_ ISBLOCKED**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) qui indique des informations sur les événements dont l’utilisation est bloquée et sur les contrôles en place.

</dd> <dt>

*RecipCount* 
</dt> <dd>

Nombre d’adresses e-mail qui reçoivent le message et qui ont des identités définies dans le champ destinataire.

</dd> <dt>

*Recipient* 
</dt> <dd>

Chaîne délimitée qui contient les noms de compte de messagerie de tous les destinataires du message.

</dd> <dt>

*AttachCount* 
</dt> <dd>

Nombre de pièces jointes au message.

</dd> <dt>

*AttachmentName* 
</dt> <dd>

Chaîne délimitée qui contient les noms de toutes les pièces jointes au message.

</dd> <dt>

*ReceivedTime* 
</dt> <dd>

Heure à laquelle le message a été tenté de recevoir.

</dd> <dt>

*EmailAccount* 
</dt> <dd>

Nom du compte de messagerie de cet utilisateur.

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

 

 




