---
description: La \_ notification SPFILENOTIFY STARTSUBQUEUE est envoyée à la fonction de rappel lorsque la file d’attente commence à traiter les opérations dans la sous-file d’attente de suppression, de renommage ou de copie.
ms.assetid: 4f971549-8f79-4995-9796-1177c3a3c416
title: Message d’SPFILENOTIFY_STARTSUBQUEUE (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 223fb54132721601633201ff34bd239c58d85cac4324970823b6a16496dbd5d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117964079"
---
# <a name="spfilenotify_startsubqueue-message"></a>\_Message SPFILENOTIFY STARTSUBQUEUE

La notification **SPFILENOTIFY \_ STARTSUBQUEUE** est envoyée à la fonction de rappel lorsque la file d’attente commence à traiter les opérations dans la sous-file d’attente de suppression, de renommage ou de copie.


```C++
SPFILENOTIFY_STARTSUBQUEUE
  Param1 = (UINT) SubQueue;
  Param2 = (UINT) NumOperations;
            
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Param1* 
</dt> <dd>

Sous-file d’attente qui a été démarrée. Ce paramètre peut prendre l’une des valeurs FILEOP \_ Delete, FILEOP \_ Rename ou FILEOP \_ Copy.

</dd> <dt>

*Param2* 
</dt> <dd>

Nombre d’opérations de copie, de renommage ou de suppression de fichiers dans la sous-file d’attente.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si une erreur se produit, la routine de rappel doit appeler [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror), en spécifiant l’erreur, puis retourner zéro. La fonction [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) retourne la **valeur false** et un appel ultérieur à [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retourne le code d’erreur défini par la routine de rappel.

Si aucune erreur ne se produit, la routine de rappel doit retourner une valeur différente de zéro.

## <a name="requirements"></a>Conditions requises



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

[**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> </dl>

 

