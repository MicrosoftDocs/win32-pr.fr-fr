---
description: Événement au niveau système généré sur un paramètre de contrôle parental modifié.
ms.assetid: 2540c3cc-96d0-4e01-a525-4da4a857cb58
title: Événement WPCEVENT_SYS_SETTINGCHANGE (Wpcevent. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7771560de0424b3a03c937e8ad2a08fdb2f23cec77fd02b6c04b29aacf16b434
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119951132"
---
# <a name="wpcevent_sys_settingchange-event"></a>\_Événement Sys \_ SETTINGCHANGE WPCEVENT

Événement au niveau système généré sur un paramètre de contrôle parental modifié.


```C++
const EVENT_DESCRIPTOR WPCEVENT_SYS_SETTINGCHANGE = {0x1, 0x0, 0x10, 0x4, 0x15, 0x1, 0x8000000000000010};
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Classe* 
</dt> <dd>

Classe qui génère l’événement.

</dd> <dt>

*Paramètre* 
</dt> <dd>

Valeur de l’énumération des **\_ paramètres WPC** .

</dd> <dt>

*Propriétaire* 
</dt> <dd>

Identificateur de sécurité de l’utilisateur qui génère l’événement.

</dd> <dt>

*OldVal* 
</dt> <dd>

Valeur précédente de ce paramètre, en cas de suppression ou de modification.

</dd> <dt>

*NewVal* 
</dt> <dd>

Nouvelle valeur de ce paramètre, si elle est ajoutée ou modifiée.

</dd> <dt>

*Motif* 
</dt> <dd>

Valeur de l’énumération [**WPCFLAG \_ ISBLOCKED**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) qui indique des informations sur les événements dont l’utilisation est bloquée et sur les contrôles en place.

</dd> <dt>

*Facultatif* 
</dt> <dd>

Champ facultatif.

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

 

 




