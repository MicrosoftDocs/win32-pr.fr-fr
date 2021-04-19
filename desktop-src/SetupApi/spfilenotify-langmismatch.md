---
description: La \_ notification SPFILENOTIFY LANGMISMATCH est envoyée à la routine de rappel si la langue du fichier à copier ne correspond pas à la langue d’un fichier cible existant.
ms.assetid: dff3969e-5847-4ad5-b7d4-237144bbe8e6
title: Message d’SPFILENOTIFY_LANGMISMATCH (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3d7828c90dd4dabb8e1cb73a8dcca7ae33ebd3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520763"
---
# <a name="spfilenotify_langmismatch-message"></a>\_Message SPFILENOTIFY LANGMISMATCH

La notification **SPFILENOTIFY \_ LANGMISMATCH** est envoyée à la routine de rappel si la langue du fichier à copier ne correspond pas à la langue d’un fichier cible existant. Elle peut être envoyée à la routine de rappel seule ou combinée, à l’aide de l’opérateur OR, avec [**SPFILENOTIFY \_ TARGETEXISTS**](spfilenotify-targetexists.md) et/ou [**SPFILENOTIFY \_ TARGETNEWER**](spfilenotify-targetnewer.md).


```C++
SPFILENOTIFY_LANGMISMATCH
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) LanguageInfo;
            
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Param1* 
</dt> <dd>

Pointeur vers une structure [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) qui contient des informations sur les chemins d’accès des fichiers source et cible.

</dd> <dt>

*Param2* 
</dt> <dd>

Identifie les langages incompatibles. Ce membre a l’identificateur de langue du fichier source dans le mot de poids faible et l’identificateur de langue du fichier cible existant dans le mot de poids fort.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La routine de rappel doit retourner l’une des valeurs suivantes.



| Code de retour                                                                          | Description                                                             |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <dt>**:**</dt> </dl>  | Copiez le fichier et remplacez le fichier existant.<br/>               |
| <dl> <dt>**FAUSSES**</dt> </dl> | Ignorez l’opération de copie. Ne pas remplacer le fichier existant.<br/> |



 

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

 

 




