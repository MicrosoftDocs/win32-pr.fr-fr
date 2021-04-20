---
title: MonthlyTrigger. RandomDelay, propriété
description: Pour les scripts, obtient ou définit un délai qui est ajouté de manière aléatoire à l’heure de début du déclencheur. | MonthlyTrigger. RandomDelay, propriété
ms.assetid: 5334356f-fef1-4d0e-9879-6ec996b75dff
keywords:
- Planificateur de tâches de la propriété RandomDelay
- Planificateur de tâches de la propriété RandomDelay, objet MonthlyTrigger
- Planificateur de tâches objet MonthlyTrigger, propriété RandomDelay
topic_type:
- apiref
api_name:
- MonthlyTrigger.RandomDelay
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa7f5c3a1831681cca2b3dc006ffb7a7d44a7a6a
ms.sourcegitcommit: b3a9abea47dea7374eac0f9a95a652ac6977fb2e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/20/2021
ms.locfileid: "107734114"
---
# <a name="monthlytriggerrandomdelay-property"></a>MonthlyTrigger. RandomDelay, propriété

Pour les scripts, obtient ou définit un délai qui est ajouté de manière aléatoire à l’heure de début du déclencheur.

## <a name="syntax"></a>Syntaxe


```VB
MonthlyTrigger.RandomDelay As String
```



## <a name="property-value"></a>Valeur de la propriété

Délai d’ajout aléatoire à l’heure de début du déclencheur. Le format de cette chaîne est `P<days>DT<hours>H<minutes>M<seconds>S` (par exemple, P2DT5S est un délai de 2 jours, 5 secondes).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                    |
| Bibliothèque de types<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MonthlyTrigger**](monthlytrigger.md)
</dt> </dl>

 

 





