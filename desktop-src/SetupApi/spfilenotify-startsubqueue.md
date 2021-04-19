---
description: La \_ notification SPFILENOTIFY STARTSUBQUEUE est envoyée à la fonction de rappel lorsque la file d’attente commence à traiter les opérations dans la sous-file d’attente de suppression, de renommage ou de copie.
ms.assetid: 4f971549-8f79-4995-9796-1177c3a3c416
title: Message d’SPFILENOTIFY_STARTSUBQUEUE (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30e4f20440c12e7fcd1900cd9762a504a26b907f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106522207"
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

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Setupapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Vue d’ensemble](overview.md)
</dt> <dt>

[Notifications](notifications.md)
</dt> <dt>

[**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> </dl>

 

