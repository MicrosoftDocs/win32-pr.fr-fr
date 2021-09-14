---
title: Élément RandomDelay (timeTriggerType)
description: Contient le délai d’attente ajouté de manière aléatoire à l’heure de début du déclencheur. | Élément RandomDelay (timeTriggerType)
ms.assetid: 84dffd18-651d-4e81-8c02-6cee9759a9b9
keywords:
- Élément RandomDelay Planificateur de tâches
topic_type:
- apiref
api_name:
- RandomDelay
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a28613cb236b6dc8a3ae77dce9452423a992a866
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126920348"
---
# <a name="randomdelay-timetriggertype-element"></a>Élément RandomDelay (timeTriggerType)

Contient le délai d’attente ajouté de manière aléatoire à l’heure de début du déclencheur. Le format de cette chaîne est PnYnMnDTnHnMnS, où nY est le nombre d’années, nM est le nombre de mois, nD le nombre de jours, 't’est le séparateur de date/heure, nH est le nombre d’heures, nM est le nombre de minutes et nS est le nombre de secondes (par exemple, PT5M spécifie 5 minutes et P1M4DT2H5M spécifie un mois, quatre jours, deux heures et cinq minutes). Pour plus d’informations sur le type de durée, consultez <https://go.microsoft.com/fwlink/p/?linkid=106886> .

``` syntax
<xs:element name="RandomDelay"
    type="duration"
    default="PT0M"
    minOccurs="0"
 />
```

L’élément est défini par le type complexe [**timeTriggerType**](taskschedulerschema-timetriggertype-complextype.md) .

## <a name="parent-element"></a>Élément parent



| Élément                                                                                    | Dérivé de                                                               | Description                                                                      |
|--------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [**TimeTrigger (triggerGroup)**](taskschedulerschema-timetrigger-triggergroup-element.md) | [**timeTriggerType**](taskschedulerschema-timetriggertype-complextype.md) | Spécifie un déclencheur qui démarre une tâche lorsque le déclencheur est activé.<br/> |



## <a name="remarks"></a>Notes

Pour le développement C++, consultez la [**propriété RandomDelay de ITimeTrigger**](/windows/desktop/api/taskschd/nf-taskschd-itimetrigger-get_randomdelay).

Pour le développement de scripts, consultez [**timetrigger. RandomDelay**](timetrigger-randomdelay.md).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



 

 





