---
description: La \_ notification SPFILENOTIFY COPYERROR est envoyée à la routine de rappel si une erreur se produit pendant une opération de copie de fichier.
ms.assetid: d6096954-c6a5-44d4-a358-c1320c50730a
title: Message d’SPFILENOTIFY_COPYERROR (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6cd44daabd6a4aed5e61a716bab3df44f35fc0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865714"
---
# <a name="spfilenotify_copyerror-message"></a>\_Message SPFILENOTIFY COPYERROR

La notification **SPFILENOTIFY \_ COPYERROR** est envoyée à la routine de rappel si une erreur se produit pendant une opération de copie de fichier.


```C++
SPFILENOTIFY_COPYERROR
  Param1 = (UINT_PTR) FilePathInfo;
  Param2 = (UINT_PTR) ReturnBuffer;
            
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Param1* 
</dt> <dd>

Pointeur vers une structure [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) .

</dd> <dt>

*Param2* 
</dt> <dd>

Pointeur vers une mémoire tampon, de taille maximale de caractères de chemin d’accès \_ , qui stocke les informations de chemin d’accès spécifiées par l’utilisateur.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Le rappel doit retourner l’une des valeurs suivantes.



| Code de retour                                                                                    | Description                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_abandon FILEOP**</dt> </dl>   | Le traitement de la file d’attente doit être annulé. [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) retourne zéro et [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retourne des informations d’erreur étendues, telles que \_ l’erreur annulée (si l’utilisateur a annulé) ou une erreur de \_ \_ mémoire insuffisante \_ .<br/> |
| <dl> <dt>**FILEOP \_ NewPath**</dt> </dl> | Recommencez l’opération de copie à l’aide du chemin d’accès de la fonction de rappel placée dans la mémoire tampon vers laquelle pointe le paramètre *param2* . La routine de rappel doit garantir que le chemin d’accès ne dépasse pas la taille de la mémoire tampon d’un tableau TCHAR d' \_ éléments de chemin d’accès max.<br/>                |
| <dl> <dt>**\_nouvelle tentative FILEOP**</dt> </dl>   | L’utilisateur tente à nouveau l’opération de copie.<br/>                                                                                                                                                                                                                   |
| <dl> <dt>**FILEOP \_ Ignorer**</dt> </dl>    | L’utilisateur ignore l’opération de copie de fichiers.<br/>                                                                                                                                                                                                                      |



 

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

 

