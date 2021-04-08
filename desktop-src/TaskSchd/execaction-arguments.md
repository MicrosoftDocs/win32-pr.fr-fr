---
title: ExecAction. arguments, propriété
description: Pour les scripts, obtient ou définit les arguments associés à l’opération de ligne de commande.
ms.assetid: 911e720f-ea7b-474d-ac75-4cd4f9adee55
keywords:
- Arguments, propriété Planificateur de tâches
- Arguments, propriété Planificateur de tâches, objet ExecAction
- Planificateur de tâches objet ExecAction, propriété arguments
topic_type:
- apiref
api_name:
- ExecAction.Arguments
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4207a9fbfb60d9e45c15e174a33e7d6ab66e5fd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941897"
---
# <a name="execactionarguments-property"></a>ExecAction. arguments, propriété

Pour les scripts, obtient ou définit les arguments associés à l’opération de ligne de commande.

## <a name="syntax"></a>Syntaxe


```VB
ExecAction.Arguments As String
```



## <a name="property-value"></a>Valeur de la propriété

Arguments requis par l’opération de ligne de commande.

## <a name="remarks"></a>Notes

Lors de la lecture ou de l’écriture de données XML, les arguments de l’opération de ligne de commande sont spécifiés dans l’élément [**arguments**](taskschedulerschema-arguments-exectype-element.md) du schéma planificateur de tâches.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                    |
| Bibliothèque de types<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ExecAction**](execaction.md)
</dt> <dt>

[Planificateur de tâches](task-scheduler-start-page.md)
</dt> </dl>

 

 





