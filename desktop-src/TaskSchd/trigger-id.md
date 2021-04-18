---
title: Propriété Trigger.Id
description: Pour les scripts, obtient ou définit l’identificateur pour le déclencheur.
ms.assetid: 15dd3aaa-f3ee-459d-a0bd-327c7a4beb03
keywords:
- Propriété ID Planificateur de tâches
- Propriété ID Planificateur de tâches, objet Trigger
- Planificateur de tâches de l’objet Trigger, propriété ID
topic_type:
- apiref
api_name:
- Trigger.Id
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91a3868f76368b19e6a316b222b8ddaf4cbbff96
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508429"
---
# <a name="triggerid-property"></a>Propriété Trigger.Id

Pour les scripts, obtient ou définit l’identificateur pour le déclencheur.

## <a name="syntax"></a>Syntaxe


```VB
Trigger.Id As String
```



## <a name="property-value"></a>Valeur de la propriété

Identificateur du déclencheur. Cet identificateur est utilisé par le Planificateur de tâches à des fins de journalisation.

## <a name="remarks"></a>Notes

Lors de la lecture ou de l’écriture de données XML pour une tâche, l’identificateur du déclencheur est spécifié dans l’attribut ID des éléments Trigger individuels (par exemple, l’attribut ID de l’élément [**BootTrigger**](taskschedulerschema-boottrigger-triggergroup-element.md) ) du schéma planificateur de tâches.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                    |
| Bibliothèque de types<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Planificateur de tâches](task-scheduler-start-page.md)
</dt> </dl>

 

 





