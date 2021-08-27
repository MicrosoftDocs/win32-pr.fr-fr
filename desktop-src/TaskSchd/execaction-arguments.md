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
ms.openlocfilehash: 899e4ceaaf3a0d04dc678592add18184401d54569fea71f0570a0acbf2a33027
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120011489"
---
# <a name="execactionarguments-property"></a>ExecAction. arguments, propriété

Pour les scripts, obtient ou définit les arguments associés à l’opération de ligne de commande.

## <a name="syntax"></a>Syntaxe


```VB
ExecAction.Arguments As String
```



## <a name="property-value"></a>Valeur de la propriété

Arguments requis par l’opération de ligne de commande.

## <a name="remarks"></a>Remarques

Lors de la lecture ou de l’écriture de données XML, les arguments de l’opération de ligne de commande sont spécifiés dans l’élément [**arguments**](taskschedulerschema-arguments-exectype-element.md) du schéma planificateur de tâches.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                    |
| Bibliothèque de types<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ExecAction**](execaction.md)
</dt> <dt>

[Planificateur de tâches](task-scheduler-start-page.md)
</dt> </dl>

 

 





