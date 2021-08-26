---
description: Événement par utilisateur généré par un client de messagerie instantanée lors de l’ajout, de la modification ou de la suppression d’informations de contact dans le contrôle parental.
ms.assetid: 0a016542-306e-48b4-8b0c-b9e4e915513e
title: Événement WPCEVENT_IM_CONTACT (Wpcevent. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: baac4bf5648b27f2e8d446a79bb2d90d52f0aac416e30d031d3b81d430a6927b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119951445"
---
# <a name="wpcevent_im_contact-event"></a>\_Événement de \_ contact WPCEVENT im

Événement par utilisateur généré par un client de messagerie instantanée lors de l’ajout, de la modification ou de la suppression d’informations de contact dans le contrôle parental.


```C++
const EVENT_DESCRIPTOR WPCEVENT_IM_CONTACT = {0xf, 0x0, 0x10, 0x4, 0x16, 0xf, 0x8000000000000030};
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*AppName* 
</dt> <dd>

Nom de l’application de messagerie instantanée qui génère l’événement.

</dd> <dt>

*AppVersion* 
</dt> <dd>

Version de l’application qui génère l’événement.

</dd> <dt>

*AccountName* 
</dt> <dd>

Nom du compte de messagerie instantanée pour cet utilisateur.

</dd> <dt>

*OldName* 
</dt> <dd>

Nom du compte de messagerie instantanée précédent, s’il a été supprimé ou modifié.

</dd> <dt>

*OldID* 
</dt> <dd>

ID associé au nom de compte de messagerie instantanée précédent.

</dd> <dt>

*NewName* 
</dt> <dd>

Nouveau nom du compte de messagerie instantanée, s’il a été ajouté ou modifié.

</dd> <dt>

*NewID* 
</dt> <dd>

ID associé au nouveau nom de compte de messagerie instantanée.

</dd> <dt>

*Motif* 
</dt> <dd>

Valeur de l’énumération [**WPCFLAG \_ ISBLOCKED**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) qui indique des informations sur les événements dont l’utilisation est bloquée et sur les contrôles en place.

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

 

 




