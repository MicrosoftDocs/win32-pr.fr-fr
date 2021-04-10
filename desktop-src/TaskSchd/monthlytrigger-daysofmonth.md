---
title: MonthlyTrigger. DaysOfMonth, propriété
description: Pour les scripts, obtient ou définit les jours du mois pendant lesquels la tâche s’exécute.
ms.assetid: 4da80d0f-ae0c-4e56-b51b-6ee6ab309d7c
keywords:
- Planificateur de tâches de la propriété DaysOfMonth
- Planificateur de tâches de la propriété DaysOfMonth, objet MonthlyTrigger
- Planificateur de tâches objet MonthlyTrigger, propriété DaysOfMonth
topic_type:
- apiref
api_name:
- MonthlyTrigger.DaysOfMonth
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81a3bd671266cfbe459218367fadf20fd52f94a7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104359"
---
# <a name="monthlytriggerdaysofmonth-property"></a>MonthlyTrigger. DaysOfMonth, propriété

Pour les scripts, obtient ou définit les jours du mois pendant lesquels la tâche s’exécute.

## <a name="syntax"></a>Syntaxe


```VB
MonthlyTrigger.DaysOfMonth As long
```



## <a name="property-value"></a>Valeur de la propriété

Un masque de bits qui indique les jours du mois pendant lesquels la tâche s’exécute.

## <a name="remarks"></a>Notes



| Jour du mois | Valeur hexadécimale  | Valeur décimale |
|--------------|------------|---------------|
| 1            | 0x01       | 1             |
| 2            | 0x02       | 2             |
| 3            | 0x04       | 4             |
| 4            | 0x08       | 8             |
| 5            | 0x10       | 16            |
| 6            | 0x20       | 32            |
| 7            | 0x40       | 64            |
| 8            | 0x80       | 128           |
| 9            | 0x100      | 256           |
| 10           | 0x200      | 512           |
| 11           | 0x400      | 1 024          |
| 12           | 0x800      | 2 048          |
| 13           | 0x1000     | 4096          |
| 14           | 0x2000     | 8 192          |
| 15           | 0x4000     | 16384         |
| 16           | 0x8000     | 32 768         |
| 17           | 0x10000    | 65536         |
| 18           | 0x20000    | 131 072        |
| 19           | 0x40000    | 262 144        |
| 20           | 0x80000    | 524 288        |
| 21           | 0x100000   | 1 048 576       |
| 22           | 0x200000   | 2 097 152       |
| 23           | 0x400000   | 4 194 304       |
| 24           | 0x800000   | 8388608       |
| 25           | 0x1000000  | 16 777 216      |
| 26           | 0x2000000  | 33554432      |
| 27           | 0x4000000  | 67108864      |
| 28           | 0x8000000  | 134217728     |
| 29           | 0x10000000 | 268435456     |
| 30           | 0x20000000 | 536870912     |
| 31           | 0x40000000 | 1073741824    |
| Dernier         | 0x80000000 | 2147483648    |



 

Lors de la lecture ou de l’écriture de vos propres données XML pour une tâche, les jours du mois sont spécifiés à l’aide de l’élément [**DaysOfMonth**](taskschedulerschema-daysofmonth-monthlyscheduletype-element.md) du schéma planificateur de tâches.

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
</dt> <dt>

[**MonthlyTrigger**](monthlytrigger.md)
</dt> </dl>

 

 





