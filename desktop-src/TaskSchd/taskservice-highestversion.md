---
title: TaskService. HighestVersion, propriété
description: Pour les scripts, indique la version la plus récente de Planificateur de tâches qu’un ordinateur prend en charge.
ms.assetid: b4e55e46-6f33-4224-811b-06bf218dd1ac
keywords:
- Planificateur de tâches de la propriété HighestVersion
- Planificateur de tâches de la propriété HighestVersion, objet TaskService
- Planificateur de tâches objet TaskService, propriété HighestVersion
topic_type:
- apiref
api_name:
- TaskService.HighestVersion
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e27618490fcf404936532d272402bebc03d94eb72ba8156e897f344b708d90ec
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119959489"
---
# <a name="taskservicehighestversion-property"></a>TaskService. HighestVersion, propriété

Pour les scripts, indique la version la plus récente de Planificateur de tâches qu’un ordinateur prend en charge.

## <a name="syntax"></a>Syntaxe


```VB
TaskService.HighestVersion As Integer
```



## <a name="property-value"></a>Valeur de la propriété

La version la plus récente de Planificateur de tâches qu’un ordinateur prend en charge. La version la plus élevée est une valeur qui est fractionnée en MajorVersion/MinorVersion sur la limite de 16 bits. Le service Planificateur de tâches retourne 1 pour la version principale et 2 pour la version mineure. Utilisez la fonction [CLng](/previous-versions//ck4c5842(v=vs.85)) pour récupérer la valeur entière de la propriété.

## <a name="examples"></a>Exemples

Le code suivant montre comment utiliser la fonction [CLng](/previous-versions//ck4c5842(v=vs.85)) pour récupérer la valeur de la propriété **HighestVersion** .


```VB
wscript.echo service.HighestVersion
Test = clng( service.HighestVersion )
If Test <> 65538  Then
    wscript.echo "Fail"

Else
    wscript.echo "Pass"
End If
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                    |
| Bibliothèque de types<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

