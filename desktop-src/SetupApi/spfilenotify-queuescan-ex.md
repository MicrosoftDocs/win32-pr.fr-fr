---
description: La \_ notification SPFILENOTIFY QUEUESCAN \_ ex est envoyée à une routine de rappel par SetupScanFileQueue pour chaque nœud dans la sous-file d’attente de copie de la file d’attente de fichiers.
ms.assetid: 293e63f9-9567-4ea7-b7e5-e5046c8a704b
title: Message d’SPFILENOTIFY_QUEUESCAN_EX (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95d151a5172918e7a7dcb13e8c480aae82da0a3ec1ffb38d26db29d63143cbc1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119992589"
---
# <a name="spfilenotify_queuescan_ex-message"></a>\_Message SPFILENOTIFY QUEUESCAN \_ ex

La notification **SPFILENOTIFY \_ QUEUESCAN \_ ex** est envoyée à une routine de rappel par [**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) pour chaque nœud dans la sous-file d’attente de copie de la file d’attente de fichiers. Cela se produit uniquement si la fonction **SetupScanFileQueue** a été appelée en spécifiant l’indicateur SPQ \_ Scan \_ use \_ CALLBACKEX.


```C++
SPFILENOTIFY_QUEUESCAN_EX
  Param1 = (PFILEPATHS) Filepaths;
            
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Param1* 
</dt> <dd>

Pointeur vers une structure [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) . Le membre **cible** est le nom du fichier cible sur le système. Le membre **source** est le chemin d’accès attendu du fichier source. Le membre **Win32Error** est l’erreur de signature.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La routine de rappel doit retourner un [code d’erreur système](/windows/desktop/Debug/system-error-codes).

Si la routine de rappel ne retourne aucune \_ erreur, l’analyse de la file d’attente continue. Si la routine retourne un autre code d’erreur, l’analyse de la file d’attente s’interrompt et [**SetupScanFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupscanfilequeuea) retourne false.

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

 

