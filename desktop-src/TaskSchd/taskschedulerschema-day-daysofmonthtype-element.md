---
title: Élément Day (daysOfMonthType)
description: Spécifie un jour du mois pendant lequel la tâche s’exécute.
ms.assetid: b213df09-9301-4a51-b000-edfdafbe861e
keywords:
- Jour, élément Planificateur de tâches
topic_type:
- apiref
api_name:
- Day
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1e8e06169d2b758264f181263a5cb717977a1602
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032588"
---
# <a name="day-daysofmonthtype-element"></a>Élément Day (daysOfMonthType)

Spécifie un jour du mois pendant lequel la tâche s’exécute.

``` syntax
<xs:element name="Day"
    type="dayOfMonthType"
 />
```

L’élément **Day** est défini par le type complexe [**daysOfMonthType**](taskschedulerschema-daysofmonthtype-complextype.md) .

## <a name="parent-element"></a>Élément parent



| Élément                                                                            | Dérivé de                                                               | Description                                                            |
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------|------------------------------------------------------------------------|
| [**DaysOfMonth**](taskschedulerschema-daysofmonth-monthlyscheduletype-element.md) | [**daysOfMonthType**](taskschedulerschema-daysofmonthtype-complextype.md) | Spécifie les jours du mois pendant lesquels la tâche est exécutée.<br/> |



## <a name="examples"></a>Exemples

Le code XML suivant définit la partie jours d’un calendrier mensuel qui exécute la tâche le 1er et le quinzième jour du mois.


```XML
<DaysOfMonth>
    <Day>1</Day>
    <Day>15</Day>
</DaysOfMonth>
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Éléments de schéma Planificateur de tâches](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





