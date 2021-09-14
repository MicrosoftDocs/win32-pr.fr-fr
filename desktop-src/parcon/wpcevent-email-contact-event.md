---
description: Événement par utilisateur généré par un client de messagerie qui enregistre la date d’ajout, de modification ou de suppression d’un contact dans le contrôle parental.
ms.assetid: 9d1f52ef-ff49-4c0d-a48a-93aeccbe7f2b
title: Événement WPCEVENT_EMAIL_CONTACT (Wpcevent. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0974030e53756b44f2be2e8550707161f2d6d461
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127235643"
---
# <a name="wpcevent_email_contact-event"></a>Événement de contact de \_ messagerie WPCEVENT \_

Événement par utilisateur généré par un client de messagerie qui enregistre la date d’ajout, de modification ou de suppression d’un contact dans le contrôle parental.


```C++
const EVENT_DESCRIPTOR WPCEVENT_EMAIL_CONTACT = {0xe, 0x0, 0x10, 0x4, 0x16, 0xe, 0x8000000000000030};
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*AppName* 
</dt> <dd>

Nom de l’application de messagerie qui génère l’événement.

</dd> <dt>

*AppVersion* 
</dt> <dd>

Version de l’application de messagerie qui génère l’événement.

</dd> <dt>

*OldName* 
</dt> <dd>

Nom du compte de messagerie précédent, s’il a été supprimé ou modifié.

</dd> <dt>

*OldID* 
</dt> <dd>

ID associé au nom du compte de messagerie précédent.

</dd> <dt>

*NewName* 
</dt> <dd>

Nouveau nom du compte de messagerie, s’il a été ajouté ou modifié.

</dd> <dt>

*NewID* 
</dt> <dd>

ID associé au nom du nouveau compte de messagerie.

</dd> <dt>

*Motif* 
</dt> <dd>

Valeur de l’énumération [**WPCFLAG \_ ISBLOCKED**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) qui indique des informations sur les événements dont l’utilisation est bloquée et sur les contrôles en place.

</dd> <dt>

*EmailAccount* 
</dt> <dd>

Nom du compte de messagerie de cet utilisateur.

</dd> </dl>

## <a name="requirements"></a>Spécifications



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

 

 




