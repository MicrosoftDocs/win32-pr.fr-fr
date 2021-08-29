---
description: La \_ notification SPFILENOTIFY NEEDMEDIA est envoyée à la routine de rappel quand un nouveau média ou un nouveau fichier cab est requis.
ms.assetid: 6a7947de-1bb3-46e0-9334-405684e58e98
title: Message d’SPFILENOTIFY_NEEDMEDIA (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ff4d65ddd4f82e1c401b157b67f39f9cc79e11b1113d502e993abe141b35d8a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119683109"
---
# <a name="spfilenotify_needmedia-message"></a>\_Message SPFILENOTIFY NEEDMEDIA

La notification **SPFILENOTIFY \_ NEEDMEDIA** est envoyée à la routine de rappel quand un nouveau média ou un nouveau fichier cab est requis.


```C++
SPFILENOTIFY_NEEDMEDIA
  Param1 = (UINT) SourceMediaInfo;
  Param2 = (UINT) NewPathInfo;
            
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Param1* 
</dt> <dd>

Pointeur vers une structure de [**\_ média source**](/windows/desktop/api/Setupapi/ns-setupapi-source_media_a) .

</dd> <dt>

*Param2* 
</dt> <dd>

Pointeur vers un tableau de caractères pour stocker les informations de chemin d’accès fournies par l’utilisateur. La taille de la mémoire tampon est un tableau **TCHAR** d' \_ éléments de chemin d’accès max. Les informations de chemin d’accès retournées par votre application d’installation ne doivent pas dépasser cette taille.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La routine de rappel doit retourner l’un des éléments suivants.



| Code de retour                                                                                    | Description                                                                                                                                                                                                             |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**FILEOP \_ NewPath**</dt> </dl> | Le média est présent et le fichier demandé est disponible dans le chemin d’accès spécifié dans la mémoire tampon pointée par *param2*.<br/>                                                                                         |
| <dl> <dt>**FILEOP \_ Ignorer**</dt> </dl>    | Ignorer le fichier demandé<br/>                                                                                                                                                                                      |
| <dl> <dt>**\_abandon FILEOP**</dt> </dl>   | Abandon du traitement de la file d’attente. La fonction [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) retourne la **valeur false**. GetLastError retourne des informations d’erreur étendues, telles que \_ l’erreur annulée si l’utilisateur a annulé.<br/> |
| <dl> <dt>**FILEOP-DOIT**</dt> </dl>     | Le média est disponible.<br/>                                                                                                                                                                                      |



 

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

[**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> <dt>

[**\_média source**](/windows/desktop/api/Setupapi/ns-setupapi-source_media_a)
</dt> </dl>

 

 




