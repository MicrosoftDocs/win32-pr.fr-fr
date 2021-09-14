---
title: RegistrationInfo. version, propriété
description: Pour les scripts, obtient ou définit le numéro de version de la tâche.
ms.assetid: 5f200948-b4ff-495c-9578-2a93b34fd75b
keywords:
- Planificateur de tâches de propriétés de version
- Propriété version Planificateur de tâches, objet RegistrationInfo
- Planificateur de tâches objet RegistrationInfo, propriété version
topic_type:
- apiref
api_name:
- RegistrationInfo.Version
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c312878383c5361317a765cbf84a503244c188a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127122845"
---
# <a name="registrationinfoversion-property"></a>RegistrationInfo. version, propriété

Pour les scripts, obtient ou définit le numéro de version de la tâche.

## <a name="syntax"></a>Syntaxe


```VB
RegistrationInfo.Version As String
```



## <a name="property-value"></a>Valeur de la propriété

Numéro de version de la tâche.

## <a name="remarks"></a>Notes

Lors de la lecture ou de l’écriture de données XML pour une tâche, le numéro de version de la tâche est spécifié à l’aide de l’élément [**version**](taskschedulerschema-version-registrationinfotype-element.md) du schéma planificateur de tâches.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                    |
| Bibliothèque de types<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Planificateur de tâches](task-scheduler-start-page.md)
</dt> </dl>

 

 





