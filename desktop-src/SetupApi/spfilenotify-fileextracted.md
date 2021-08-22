---
description: La \_ notification SPFILENOTIFY FILEEXTRACTED est envoyée à une routine de rappel par SetupIterateCabinet pour indiquer qu’un fichier a été extrait du fichier CAB ou qu’une extraction a échoué et que le traitement de l’armoire a été annulé.
ms.assetid: 70ffe06c-e72d-4bb8-a13c-e2946ff72fa6
title: Message d’SPFILENOTIFY_FILEEXTRACTED (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56b5028dec11cf2317be080fb82b79bf155be007c66abcbee33492aa229d6317
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119665109"
---
# <a name="spfilenotify_fileextracted-message"></a>\_Message SPFILENOTIFY FILEEXTRACTED

La notification **SPFILENOTIFY \_ FILEEXTRACTED** est envoyée à une routine de rappel par [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) pour indiquer qu’un fichier a été extrait du fichier CAB ou qu’une extraction a échoué et que le traitement de l’armoire a été annulé.


```C++
SPFILENOTIFY_FILEEXTRACTED
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Param1* 
</dt> <dd>

Pointeur vers une structure [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) qui contient des informations de chemin d’accès pour le fichier extrait. Le membre **sourceFile** de la structure **FILEPATHS** contient le chemin d’accès source complet du fichier CAB. Le membre **TargetFile** fournit le chemin d’accès cible complet du fichier à installer sur le système.

</dd> <dt>

*Param2* 
</dt> <dd>

Inutilisé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La routine de rappel du fichier cab doit retourner l’une des valeurs suivantes.



| Code de retour                                                                               | Description                                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**AUCUNE \_ erreur**</dt> </dl>  | Aucune erreur ne s’est produite. poursuivez le traitement du fichier CAB.<br/>                                                                                                                                |
| <dl> <dt>**ERREUR \_ xxx**</dt> </dl> | Une erreur du type spécifié s’est produite. [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) retourne la valeur zéro. [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retourne le code d’erreur spécifié.<br/> |



 

> [!Note]  
> Aucune routine de rappel d’armoire par défaut n’est fournie avec l’API d’installation. Votre application de configuration doit fournir une routine de rappel pour gérer les notifications envoyées par la fonction [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) .

 

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

[**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta)
</dt> </dl>

 

