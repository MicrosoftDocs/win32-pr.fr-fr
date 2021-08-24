---
description: Événement par utilisateur généré par un client de messagerie instantanée quand des fonctionnalités définies sont utilisées dans le contrôle parental.
ms.assetid: 45e80314-90b1-4fcf-9c8f-c9840ae1775b
title: Événement WPCEVENT_IM_FEATURE (Wpcevent. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8046e755540a2282e84ea25c5278cf0c0b113264e78a3db31b6bd8a42de599cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119951440"
---
# <a name="wpcevent_im_feature-event"></a>\_Événement de fonctionnalité de messagerie instantanée WPCEVENT \_

Événement par utilisateur généré par un client de messagerie instantanée quand des fonctionnalités définies sont utilisées dans le contrôle parental.


```C++
const EVENT_DESCRIPTOR WPCEVENT_IM_FEATURE = {0xb, 0x0, 0x10, 0x4, 0x16, 0xb, 0x8000000000000030};
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*AppName* 
</dt> <dd>

Nom de l’application de messagerie instantanée.

</dd> <dt>

*AppVersion* 
</dt> <dd>

Chaîne de version de l’application.

</dd> <dt>

*AccountName* 
</dt> <dd>

Nom du compte de messagerie instantanée de cet utilisateur.

</dd> <dt>

*ConvID* 
</dt> <dd>

ID de cette conversation.

</dd> <dt>

*MediaType* 
</dt> <dd>

Valeur de l’énumération de la [**\_ \_ fonctionnalité de messagerie instantanée WPCFLAG**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_im_feature) qui indique des informations sur les fonctionnalités accessibles pendant une interaction de messagerie instantanée.

</dd> <dt>

*Motif* 
</dt> <dd>

Valeur de l’énumération [**WPCFLAG \_ ISBLOCKED**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) qui indique des informations sur les événements dont l’utilisation est bloquée et sur les contrôles en place.

</dd> <dt>

*RecipCount* 
</dt> <dd>

Nombre d’utilisateurs de messagerie instantanée qui reçoivent la fonctionnalité et qui ont des identités définies dans le champ destinataire.

</dd> <dt>

*Recipient* 
</dt> <dd>

Chaîne délimitée qui contient les identités de compte de messagerie instantanée de tous les utilisateurs qui reçoivent la fonctionnalité.

</dd> <dt>

*Expéditeur* 
</dt> <dd>

Nom du compte de messagerie instantanée pour l’utilisateur qui est propriétaire de la fonctionnalité.

</dd> <dt>

*SenderIP* 
</dt> <dd>

L’adresse IP de l’ordinateur de l’expéditeur.

</dd> <dt>

*Données* 
</dt> <dd>

Description des données dans la fonctionnalité.

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

 

 




