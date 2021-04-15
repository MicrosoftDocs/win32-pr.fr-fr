---
description: La \_ notification SPFILENOTIFY STARTDELETE est envoyée à la fonction de rappel lorsque la file d’attente démarre une opération de suppression de fichier.
ms.assetid: 244714ad-dde7-4b5a-b3f3-78aa4cc901f5
title: Message d’SPFILENOTIFY_STARTDELETE (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a4a0d362a1c1c3824154fb02e0bb9cf01b24d16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529770"
---
# <a name="spfilenotify_startdelete-message"></a>\_Message SPFILENOTIFY STARTDELETE

La notification **SPFILENOTIFY \_ STARTDELETE** est envoyée à la fonction de rappel lorsque la file d’attente démarre une opération de suppression de fichier.


```C++
SPFILENOTIFY_STARTDELETE
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

A toujours la valeur FILEOP \_ Delete.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La routine de rappel doit retourner l’une des valeurs suivantes.



| Code de retour                                                                                  | Description                                                                                                                                                                                                                                                                                                                                                                  |
|----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_abandon FILEOP**</dt> </dl> | Abandonner la validation de la file d’attente. La routine de rappel doit appeler [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror) pour indiquer la raison de l’abandon. [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) retourne **false** et un appel ultérieur à [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retourne le code d’erreur défini par la routine de rappel lors de l’appel à **SetLastError**.<br/> |
| <dl> <dt>**FILEOP \_ doit**</dt> </dl>  | Effectuez l’opération de copie de fichiers.<br/>                                                                                                                                                                                                                                                                                                                                  |
| <dl> <dt>**FILEOP \_ Ignorer**</dt> </dl>  | Ignorer l’opération de copie en cours.<br/>                                                                                                                                                                                                                                                                                                                                  |



 

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

 

