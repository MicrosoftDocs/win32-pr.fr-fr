---
description: La \_ notification SPFILENOTIFY TARGETNEWER est envoyée à la routine de rappel si le fichier à copier a été mis en file d’attente avec les indicateurs plus récents de la \_ copie SP \_ plus récente ou de la \_ copie SP \_ \_ , et qu’une version plus récente du fichier existe déjà dans le répertoire cible.
ms.assetid: 93bcd610-f75d-4900-841c-f67946af5c4a
title: Message d’SPFILENOTIFY_TARGETNEWER (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c432515a5ce0e9a1eddb8ea6e92f7376c318b4f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106542948"
---
# <a name="spfilenotify_targetnewer-message"></a>\_Message SPFILENOTIFY TARGETNEWER

La notification **SPFILENOTIFY \_ TARGETNEWER** est envoyée à la routine de rappel si le fichier à copier a été mis en file d’attente avec les indicateurs plus récents de la \_ copie SP \_ plus récente ou de la \_ copie SP \_ \_ , et qu’une version plus récente du fichier existe déjà dans le répertoire cible. Elle peut être envoyée à la routine de rappel seule ou associée à [**SPFILENOTIFY \_ LANGMISMATCH**](spfilenotify-langmismatch.md) et/ou [**SPFILENOTIFY \_ TARGETEXISTS**](spfilenotify-targetexists.md).


```C++
SPFILENOTIFY_TARGETNEWER
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Param1* 
</dt> <dd>

Pointeur vers une structure [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) qui contient des informations sur les chemins d’accès pour les fichiers source et cible.

</dd> <dt>

*Param2* 
</dt> <dd>

Ce paramètre n’est pas utilisé, sauf si cette notification est combinée, à l’aide de l’opérateur OR, avec [**SPFILENOTIFY \_ LANGMISMATCH**](spfilenotify-langmismatch.md).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La routine de rappel doit retourner l’une des valeurs suivantes.



| Code de retour                                                                          | Description                                            |
|--------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <dt>**:**</dt> </dl>  | Remplacez le fichier dans le répertoire cible.<br/> |
| <dl> <dt>**FAUSSES**</dt> </dl> | Ignorer l’opération de copie en cours.<br/>            |



 

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
</dt> <dt>

[**SetupInstallFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilea)
</dt> <dt>

[**SetupInstallFileEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfileexa)
</dt> <dt>

[**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona)
</dt> </dl>

 

 




