---
description: Événement par utilisateur généré par un client de messagerie instantanée lors de l’ajout, de la modification ou de la suppression d’informations de contact dans le contrôle parental.
ms.assetid: 0a016542-306e-48b4-8b0c-b9e4e915513e
title: Événement WPCEVENT_IM_CONTACT (Wpcevent. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9747f7ede57f7a1d77af0f0e8e5425401ee32b36
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210477"
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
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                             |
| En-tête<br/>                   | <dl> <dt>Wpcevent. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Utilisation des API de journalisation pour les contrôles parentaux](using-logging-apis-for-parental-controls.md)
</dt> <dt>

[**WPC \_ args \_ CONVERSATIONINITEVENT**](/windows/win32/api/wpcevent/ne-wpcevent-wpc_args_conversationinitevent)
</dt> </dl>

 

 




