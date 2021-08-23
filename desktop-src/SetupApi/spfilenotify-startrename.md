---
description: La \_ notification SPFILENOTIFY STARTRENAME est envoyée à la fonction de rappel lorsque la file d’attente démarre une opération de changement de nom de fichier.
ms.assetid: 005c1840-6aa9-4e94-bfe7-6a9d53735fd9
title: Message d’SPFILENOTIFY_STARTRENAME (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ec75c84841adf5cb8a187e8d8431f031af74b31f33af7a87e46225b1e9a3464
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119739419"
---
# <a name="spfilenotify_startrename-message"></a>\_Message SPFILENOTIFY STARTRENAME

La notification **SPFILENOTIFY \_ STARTRENAME** est envoyée à la fonction de rappel lorsque la file d’attente démarre une opération de changement de nom de fichier.


```C++
SPFILENOTIFY_STARTRENAME
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) Operation;
            
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Param1* 
</dt> <dd>

Pointeur vers une structure [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) .

</dd> <dt>

*Param2* 
</dt> <dd>

A toujours la valeur FILEOP \_ Rename.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La routine de rappel doit retourner l’une des valeurs suivantes.



| Code de retour                                                                                  | Description                                                                                                                                                                                                                                                                                                                                                                     |
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_abandon FILEOP**</dt> </dl> | Abandonner la validation de la file d’attente. La routine de rappel doit appeler [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror) pour indiquer la raison de l’arrêt. [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) retourne **false** et un appel ultérieur à [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retourne le code d’erreur défini par la routine de rappel lors de l’appel à **SetLastError**.<br/> |
| <dl> <dt>**FILEOP \_ doit**</dt> </dl>  | Effectuez l’opération de copie de fichiers.<br/>                                                                                                                                                                                                                                                                                                                                     |
| <dl> <dt>**FILEOP \_ Ignorer**</dt> </dl>  | Ignorer l’opération de copie en cours.<br/>                                                                                                                                                                                                                                                                                                                                     |



 

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

 

