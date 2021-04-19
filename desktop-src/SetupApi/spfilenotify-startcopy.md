---
description: La \_ notification SPFILENOTIFY STARTCOPY est envoyée à la fonction de rappel lorsque la file d’attente démarre une opération de copie de fichiers.
ms.assetid: 01a7d9d4-b548-4e72-b1c9-7116e67c023b
title: Message d’SPFILENOTIFY_STARTCOPY (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6693938a2f67530e7e3c906c5105d2c98a915a32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106529356"
---
# <a name="spfilenotify_startcopy-message"></a>\_Message SPFILENOTIFY STARTCOPY

La notification **SPFILENOTIFY \_ STARTCOPY** est envoyée à la fonction de rappel lorsque la file d’attente démarre une opération de copie de fichiers.


```C++
SPFILENOTIFY_STARTCOPY
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

A toujours la valeur FILEOP \_ Copy.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La routine de rappel doit retourner l’une des valeurs suivantes.



| Code de retour                                                                                  | Description                                                                                                                                                                                                                                                                                                                                                                                          |
|----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_abandon FILEOP**</dt> </dl> | Abandonner le processus de validation de la file d’attente. La routine de rappel doit appeler [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror) pour indiquer la raison de l’arrêt. La fonction [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) retourne la **valeur false** et un appel ultérieur à [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retourne le code d’erreur défini par la routine de rappel lors de l’appel à **SetLastError**.<br/> |
| <dl> <dt>**FILEOP \_ doit**</dt> </dl>  | Effectuez l’opération de copie de fichiers.<br/>                                                                                                                                                                                                                                                                                                                                                          |
| <dl> <dt>**FILEOP \_ Ignorer**</dt> </dl>  | Ignorer l’opération de copie en cours.<br/>                                                                                                                                                                                                                                                                                                                                                          |



 

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

[**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)
</dt> <dt>

[**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> </dl>

 

