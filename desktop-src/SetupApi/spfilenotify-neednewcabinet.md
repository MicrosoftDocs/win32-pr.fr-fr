---
description: La \_ notification SPFILENOTIFY NEEDNEWCABINET est envoyée par SetupIterateCabinet pour indiquer que le fichier actuel continue dans une autre armoire.
ms.assetid: 01207429-11fb-4e2c-89ba-54321992e953
title: Message d’SPFILENOTIFY_NEEDNEWCABINET (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3187d48b89579c329a4d0163e151824288462344
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210423"
---
# <a name="spfilenotify_neednewcabinet-message"></a>\_Message SPFILENOTIFY NEEDNEWCABINET

La notification **SPFILENOTIFY \_ NEEDNEWCABINET** est envoyée par [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) pour indiquer que le fichier actuel continue dans une autre armoire. Votre routine de rappel peut ensuite appeler [**SetupPromptForDisk**](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptfordiska)ou créer sa propre boîte de dialogue pour inviter l’utilisateur à insérer le disque suivant.


```C++
SPFILENOTIFY_NEEDNEWCABINET
  Param1 = (UINT) CabinetInfo;
  Param2 = (UINT) NewPath;
            
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Param1* 
</dt> <dd>

Pointeur vers une structure d' [**\_ informations d’armoire**](/windows/desktop/api/Setupapi/ns-setupapi-cabinet_info_a) qui contient des informations sur l’armoire et le fichier à extraire.

</dd> <dt>

*Param2* 
</dt> <dd>

Si le rappel ne retourne aucune \_ erreur, ce paramètre est un pointeur vers une chaîne terminée par le caractère null. Si la chaîne n’est pas vide, elle spécifie un nouveau chemin d’accès au fichier CAB.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Votre routine doit retourner l’une des valeurs suivantes.



| Code de retour                                                                                 | Description                                                                                                                                                                                                                                  |
|---------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**AUCUNE \_ erreur**</dt> </dl>    | Aucune erreur ne s’est produite. poursuivez le traitement du fichier CAB.<br/>                                                                                                                                                                        |
| <dl> <dt>**Erreur \_* XXX * * *</dt> </dl> | Une erreur du type spécifié s’est produite. La fonction [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) retourne la **valeur false** et le code d’erreur spécifié est retourné par un appel à [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).<br/> |



 

> [!Note]  
> Il n’existe aucune routine de rappel d’armoire par défaut ; par conséquent, vous devez fournir une routine de rappel pour gérer les notifications envoyées par [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta).

 

## <a name="remarks"></a>Notes

Si la routine de rappel ne retourne aucune \_ erreur, [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) vérifie la mémoire tampon désignée par *param2*. Si la mémoire tampon n’est pas vide, elle contient un nouveau chemin d’accès source. Si la mémoire tampon est vide, le chemin d’accès source est supposé être inchangé.

Votre fonction de rappel doit s’assurer que le fichier cab est accessible avant de retourner, en appelant la fonction [**SetupPromptForDisk**](/windows/desktop/api/Setupapi/nf-setupapi-setuppromptfordiska) , si un nouveau support doit être inséré.

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

[**\_infos sur le cabinet**](/windows/desktop/api/Setupapi/ns-setupapi-cabinet_info_a)
</dt> <dt>

[**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta)
</dt> </dl>

 

