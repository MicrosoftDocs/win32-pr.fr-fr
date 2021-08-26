---
description: Événement par utilisateur généré par un client de messagerie qui enregistre la date d’ajout, de modification ou de suppression d’un contact dans le contrôle parental.
ms.assetid: 9d1f52ef-ff49-4c0d-a48a-93aeccbe7f2b
title: Événement WPCEVENT_EMAIL_CONTACT (Wpcevent. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d84a450c53705dae2db777081f7177f43505e0481ae38a67c1b90e507fa4a5d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119951569"
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

 

 




