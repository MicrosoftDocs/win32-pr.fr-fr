---
title: Élément Delay (bootTriggerType)
description: Spécifie la durée entre le démarrage du système et le démarrage de la tâche.
ms.assetid: 2a583069-ad38-43b4-bcf2-f7c9101f1927
keywords:
- Retarder l’élément Planificateur de tâches
topic_type:
- apiref
api_name:
- Delay
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 91789b22b992af163e9676ef156a2a72f4316ac49b9b47b30ae5599446918bed
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119334599"
---
# <a name="delay-boottriggertype-element"></a>Élément Delay (bootTriggerType)

Spécifie la durée entre le démarrage du système et le démarrage de la tâche. Le format de cette chaîne est PnYnMnDTnHnMnS, où nY est le nombre d’années, nM est le nombre de mois, nD le nombre de jours, 't’est le séparateur de date/heure, nH est le nombre d’heures, nM est le nombre de minutes et nS est le nombre de secondes (par exemple, PT5M spécifie 5 minutes et P1M4DT2H5M spécifie un mois, quatre jours, deux heures et cinq minutes). Pour plus d’informations sur le type de durée, consultez <https://go.microsoft.com/fwlink/p/?linkid=106886> .

``` syntax
<xs:element name="Delay"
    type="duration"
 />
```

L’élément **delay** est défini par le type complexe [**bootTriggerType**](taskschedulerschema-boottriggertype-complextype.md) .

## <a name="parent-element"></a>Élément parent



| Élément                                                                     | Dérivé de                                                               | Description                                                                  |
|-----------------------------------------------------------------------------|----------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [**BootTrigger**](taskschedulerschema-boottrigger-triggergroup-element.md) | [**bootTriggerType**](taskschedulerschema-boottriggertype-complextype.md) | Spécifie un déclencheur qui démarre une tâche au démarrage du système.<br/> |



## <a name="remarks"></a>Remarques

Pour le développement de scripts, le délai de déclenchement des événements est spécifié par la propriété [**BootTrigger. Delay**](boottrigger-delay.md) .

Pour le développement C++, le délai de déclenchement des événements est spécifié par la propriété [**IBootTrigger ::D Nouv**](/windows/desktop/api/taskschd/nf-taskschd-iboottrigger-get_delay) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Éléments de schéma Planificateur de tâches](task-scheduler-schema-elements.md)
</dt> <dt>

[Planificateur de tâches](task-scheduler-start-page.md)
</dt> </dl>

 

 





