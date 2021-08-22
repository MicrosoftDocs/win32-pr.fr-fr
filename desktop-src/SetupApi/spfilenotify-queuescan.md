---
description: La \_ notification SPFILENOTIFY QUEUESCAN est envoyée à une routine de rappel par SetupScanFileQueue pour chaque nœud dans la sous-file d’attente de copie de la file d’attente de fichiers. Cela se produit uniquement si la fonction SetupScanFileQueue a été appelée en spécifiant le rappel d’utilisation de l’indicateur SPQ \_ Scan \_ \_ .
ms.assetid: 8aacc6c0-b6fe-4b4a-bbe4-a0351baf1f30
title: Message d’SPFILENOTIFY_QUEUESCAN (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ab9c680ff2aaa3056ab74db741a34bb9f0379ec7123821b1de4c20200997ab6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119664849"
---
# <a name="spfilenotify_queuescan-message"></a>\_Message SPFILENOTIFY QUEUESCAN

La notification **SPFILENOTIFY \_ QUEUESCAN** est envoyée à une routine de rappel par [**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) pour chaque nœud dans la sous-file d’attente de copie de la file d’attente de fichiers. Cela se produit uniquement si la fonction **SetupScanFileQueue** a été appelée en spécifiant le rappel d’utilisation de l’indicateur SPQ \_ Scan \_ \_ .


```C++
SPFILENOTIFY_QUEUESCAN
  Param1 = (UINT) TargetPath;
  Param2 = (UINT) DelayFlag;
            
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Param1* 
</dt> <dd>

Chaîne terminée par le caractère null qui spécifie les informations de chemin d’accès cible pour le fichier mis en file d’attente dans le nœud actuel.

</dd> <dt>

*Param2* 
</dt> <dd>

Si le fichier du nœud actuel de la file d’attente est en cours d’utilisation, *param2* prend la valeur SPQ \_ retardée \_ . Si le fichier n’est pas utilisé, la valeur est égale à zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La routine de rappel doit retourner un [code d’erreur système](/windows/desktop/Debug/system-error-codes).

Si la routine de rappel ne retourne aucune \_ erreur, l’analyse de la file d’attente continue. Si la routine retourne un autre code d’erreur, l’analyse de la file d’attente s’interrompt et [**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) retourne **false**.

> [!Note]  
> Cette notification n’est pas gérée par la fonction [**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka) .

 

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

[**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea)
</dt> </dl>

 

