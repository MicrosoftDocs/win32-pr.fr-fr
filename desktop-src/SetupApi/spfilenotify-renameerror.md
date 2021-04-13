---
description: La \_ notification SPFILENOTIFY RENAMEERROR est envoyée à la routine de rappel si une erreur se produit pendant une opération de changement de nom de fichier.
ms.assetid: b7016cbe-2987-477f-958b-52b7a31c54c2
title: Message d’SPFILENOTIFY_RENAMEERROR (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79a45658153980d7cfd5cb99b76fb344fcdb4bd8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319874"
---
# <a name="spfilenotify_renameerror-message"></a>\_Message SPFILENOTIFY RENAMEERROR

La notification **SPFILENOTIFY \_ RENAMEERROR** est envoyée à la routine de rappel si une erreur se produit pendant une opération de changement de nom de fichier.


```C++
SPFILENOTIFY_RENAMEERROR
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Param1* 
</dt> <dd>

Pointeur vers une structure [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) . Le membre **Win32Error** de la structure **FILEPATHS** spécifie l’erreur qui s’est produite pendant l’opération de changement de nom.

</dd> <dt>

*Param2* 
</dt> <dd>

Inutilisé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La routine de rappel doit retourner l’un des éléments suivants.



| Code de retour                                                                                  | Description                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_nouvelle tentative FILEOP**</dt> </dl> | L’utilisateur a choisi de retenter l’opération de changement de nom.<br/>                                                                                                                                                                                                  |
| <dl> <dt>**FILEOP \_ Ignorer**</dt> </dl>  | L’utilisateur a choisi d’ignorer l’opération de changement de nom de fichier.<br/>                                                                                                                                                                                                      |
| <dl> <dt>**\_abandon FILEOP**</dt> </dl> | Arrêtez la validation de la file d’attente. [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) retourne **false**. [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retourne des informations d’erreur étendues, telles que \_ l’erreur annulée (si l’utilisateur a annulé) ou une erreur de \_ \_ mémoire insuffisante \_ .<br/> |



 

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

 

