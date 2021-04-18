---
title: Objet TaskNamedValuePair
description: Objet de script utilisé pour créer une paire nom-valeur dans laquelle le nom est associé à la valeur.
ms.assetid: def679b1-28d5-4c52-9dca-42a6de06a1ec
keywords:
- Objet TaskNamedValuePair Planificateur de tâches
- Planificateur de tâches d’objets TaskNamedValuePair, Description
topic_type:
- apiref
api_name:
- TaskNamedValuePair
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b95229b5714d2cdcc43a071f2e51a50e04706429
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512786"
---
# <a name="tasknamedvaluepair-object"></a>Objet TaskNamedValuePair

Objet de script utilisé pour créer une paire nom-valeur dans laquelle le nom est associé à la valeur.

## <a name="members"></a>Membres

L’objet **TaskNamedValuePair** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

L’objet **TaskNamedValuePair** a ces propriétés.



| Propriété                                             | Description                                                                            |
|:-----------------------------------------------------|:---------------------------------------------------------------------------------------|
| [**Nom**](tasknamedvaluepair-name.md)<br/>   | Obtient ou définit le nom associé à une valeur dans une paire nom-valeur.<br/> |
| [**Valeur**](tasknamedvaluepair-value.md)<br/> | Obtient ou définit la valeur associée à un nom dans une paire nom-valeur.<br/> |



 

## <a name="remarks"></a>Notes

Lors de la lecture ou de l’écriture de votre propre XML pour une tâche, une paire nom-valeur est spécifiée à l’aide de l’élément [**ValueQueries**](taskschedulerschema-valuequeries-eventtriggertype-element.md) du schéma planificateur de tâches.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                    |
| Bibliothèque de types<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**TaskNamedValueCollection**](tasknamedvaluecollection.md)
</dt> </dl>

 

 





