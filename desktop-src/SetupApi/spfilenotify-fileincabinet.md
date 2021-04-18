---
description: La \_ notification SPFILENOTIFY FILEINCABINET est envoyée à une routine de rappel par SetupIterateCabinet pour chaque fichier trouvé dans le fichier CAB. La routine de rappel doit retourner une valeur indiquant s’il faut extraire le fichier.
ms.assetid: c6d89759-c0d4-4741-b992-43eaa0dc4f01
title: Message d’SPFILENOTIFY_FILEINCABINET (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 496db3cef814f2bf366f4cb6f91132efe01a2406
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106526301"
---
# <a name="spfilenotify_fileincabinet-message"></a>\_Message SPFILENOTIFY FILEINCABINET

La notification **SPFILENOTIFY \_ FILEINCABINET** est envoyée à une routine de rappel par [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) pour chaque fichier trouvé dans le fichier CAB. La routine de rappel doit retourner une valeur indiquant s’il faut extraire le fichier.


```C++
SPFILENOTIFY_FILEINCABINET
  Param1 = (UINT) FileInCabinetInfo;
  Param2 = (UINT) CabinetFile;
            
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Param1* 
</dt> <dd>

Pointeur vers un [**fichier dans la structure d' \_ \_ \_ informations**](/windows/desktop/api/Setupapi/ns-setupapi-file_in_cabinet_info_a) du fichier CAB qui contient des informations sur le fichier dans le cabinet.

</dd> <dt>

*Param2* 
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui contient le nom de fichier du fichier CAB.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Votre routine de rappel doit retourner l’un des éléments suivants.



| Code de retour                                                                                 | Description                                  |
|---------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**FILEOP \_ Ignorer**</dt> </dl> | N’extrayez pas le fichier, ignorez-le.<br/> |
| <dl> <dt>**FILEOP \_ doit**</dt> </dl> | Extrayez le fichier.<br/>                 |



 

Si votre routine de rappel retourne FILEOP \_ doit, le nom à utiliser pour le fichier extrait doit être spécifié dans le membre **FullTargetName** du [**fichier dans la structure d' \_ \_ \_ informations du fichier CAB**](/windows/desktop/api/Setupapi/ns-setupapi-file_in_cabinet_info_a) passé à la routine dans *param1*.

> [!Note]  
> Il n’existe aucune routine de rappel d’armoire par défaut. L’application d’installation doit fournir une routine de rappel pour gérer les notifications envoyées par [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta).

 

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

[**fichier \_ dans le fichier \_ CAB \_**](/windows/desktop/api/Setupapi/ns-setupapi-file_in_cabinet_info_a)
</dt> <dt>

[**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta)
</dt> </dl>

 

 




