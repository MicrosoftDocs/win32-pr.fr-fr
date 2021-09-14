---
description: Événement par utilisateur généré par le filtre de contenu Web en raison d’une tentative d’accès à une URL.
ms.assetid: 636b0ce8-cf08-4536-9b41-79512b02a066
title: Événement WPCEVENT_WEB_URLVISIT (Wpcevent. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1075ae930cdaa9ee539dbc17a8c13d5c2a41add
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127235614"
---
# <a name="wpcevent_web_urlvisit-event"></a>\_ \_ Événement URLVISIT Web WPCEVENT

Événement par utilisateur généré par le filtre de contenu Web en raison d’une tentative d’accès à une URL.


```C++
const EVENT_DESCRIPTOR WPCEVENT_WEB_URLVISIT = {0x3, 0x0, 0x10, 0x4, 0x18, 0x3, 0x8000000000000010};
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*URL* 
</dt> <dd>

URL qui tente d’être ouverte.

</dd> <dt>

*Application* 
</dt> <dd>

L’application qui génère l’événement.

</dd> <dt>

*Version* 
</dt> <dd>

Chaîne de version de l’application.

</dd> <dt>

*Motif* 
</dt> <dd>

Valeur de l’énumération [**WPCFLAG \_ ISBLOCKED**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) qui indique des informations sur les événements dont l’utilisation est bloquée et sur les contrôles en place.

</dd> <dt>

*RatingSystemID* 
</dt> <dd>

GUID qui identifie le système d’évaluation actuel.

</dd> <dt>

*CatCount* 
</dt> <dd>

Nombre d’entrées bloquées dans le champ de catégorie.

</dd> <dt>

*Catégorie* 
</dt> <dd>

Chaîne délimitée d’identificateurs de catégorie qui sont bloqués.

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

 

 




