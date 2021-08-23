---
description: La \_ notification SPFILENOTIFY TARGETEXISTS est envoyée à la routine de rappel si le fichier à copier a été mis en file d’attente avec l' \_ indicateur SP Copy \_ NOOVERWRITE et que ce fichier existe déjà dans le répertoire cible.
ms.assetid: 5c6e0c59-0340-4aa6-94db-8d9a5d202758
title: Message d’SPFILENOTIFY_TARGETEXISTS (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c51f845d7ccb41b330f6365eff269645d08e58597e7e6dd3e9acc7a7f0300c80
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119664739"
---
# <a name="spfilenotify_targetexists-message"></a>\_Message SPFILENOTIFY TARGETEXISTS

La notification **SPFILENOTIFY \_ TARGETEXISTS** est envoyée à la routine de rappel si le fichier à copier a été mis en file d’attente avec l' \_ indicateur SP Copy \_ NOOVERWRITE et que ce fichier existe déjà dans le répertoire cible. Elle peut être envoyée à la routine de rappel seule ou combinée, à l’aide de l’opérateur OR, avec les notifications [**SPFILENOTIFY \_ LANGMISMATCH**](spfilenotify-langmismatch.md) et/ou [**SPFILENOTIFY \_ TARGETNEWER**](spfilenotify-targetnewer.md) .


```C++
SPFILENOTIFY_TARGETEXISTS
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

Ce paramètre n’est pas utilisé, sauf si cette notification est combinée, à l’aide de l’opérateur OR, avec la notification [**SPFILENOTIFY \_ LANGMISMATCH**](spfilenotify-langmismatch.md) .

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
</dt> <dt>

[**SetupInstallFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilea)
</dt> <dt>

[**SetupInstallFileEx**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfileexa)
</dt> <dt>

[**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona)
</dt> </dl>

 

 




