---
description: La \_ notification SPFILENOTIFY ENDCOPY est passée à la fonction de rappel lorsque la file d’attente termine une opération de copie. Cette notification est envoyée même si l’utilisateur annule ou si une erreur se produit.
ms.assetid: d58dc397-8803-466c-9069-728faf2c2030
title: Message d’SPFILENOTIFY_ENDCOPY (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b87b4a53e1dc88f8cdb7d2ec790cab82b66d8698c6f45abf97e2b5ac5b8511ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119665129"
---
# <a name="spfilenotify_endcopy-message"></a>\_Message SPFILENOTIFY ENDCOPY

La notification **SPFILENOTIFY \_ ENDCOPY** est passée à la fonction de rappel lorsque la file d’attente termine une opération de copie. Cette notification est envoyée même si l’utilisateur annule ou si une erreur se produit.


```C++
SPFILENOTIFY_ENDCOPY
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Param1* 
</dt> <dd>

Pointeur vers une structure [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) . Le membre **Win32Error** de la structure **FILEPATHS** indique le résultat de l’opération de copie.

</dd> <dt>

*Param2* 
</dt> <dd>

Inutilisé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Le code de retour est ignoré.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Setupapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Vue d'ensemble](overview.md)
</dt> <dt>

[Notifications](notifications.md)
</dt> <dt>

[**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)
</dt> <dt>

[**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> </dl>

 

 




