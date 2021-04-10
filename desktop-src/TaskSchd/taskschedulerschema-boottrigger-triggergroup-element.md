---
title: Élément BootTrigger (triggerGroup)
description: Spécifie un déclencheur qui démarre une tâche au démarrage du système.
ms.assetid: c6833547-0daf-4e8a-b8c5-b422827b1d96
keywords:
- déclencheur de démarrage Planificateur de tâches, élément XML
- Élément BootTrigger Planificateur de tâches
topic_type:
- apiref
api_name:
- BootTrigger
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: eb6ccf590893e19340662fd4c47e4aa68047b29d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317357"
---
# <a name="boottrigger-triggergroup-element"></a>Élément BootTrigger (triggerGroup)

Spécifie un déclencheur qui démarre une tâche au démarrage du système.

``` syntax
<xs:element name="BootTrigger"
    type="bootTriggerType"
 />
```

L’élément **BootTrigger** est défini par le type complexe [**bootTriggerType**](taskschedulerschema-boottriggertype-complextype.md) .

## <a name="parent-element"></a>Élément parent



| Élément                                                           | Dérivé de                                                         | Description                                            |
|-------------------------------------------------------------------|----------------------------------------------------------------------|--------------------------------------------------------|
| [**Déclencheurs**](taskschedulerschema-triggers-tasktype-element.md) | [**triggersType**](taskschedulerschema-triggerstype-complextype.md) | Spécifie les déclencheurs qui démarrent la tâche.<br/> |



## <a name="child-elements"></a>Éléments enfants



| Élément                                                                                                        | Type                                                                     | Description                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [**Délai (bootTriggerType)**](taskschedulerschema-delay-boottriggertype-element.md)                           | duration                                                                 | Spécifie la durée entre le démarrage du système et le démarrage de la tâche.<br/>                            |
| [**Activé (triggerBaseType)**](taskschedulerschema-enabled-triggerbasetype-element.md)                       | boolean                                                                  | Spécifie que le déclencheur est activé.<br/>                                                                                  |
| [**EndBoundary (triggerBaseType)**](taskschedulerschema-endboundary-triggerbasetype-element.md)               | dateTime                                                                 | Spécifie la date et l’heure de désactivation du déclencheur. Le déclencheur ne peut pas démarrer la tâche une fois qu’elle est désactivée.<br/> |
| [**ExecutionTimeLimit (triggerBaseType)**](taskschedulerschema-executiontimelimit-triggerbasetype-element.md) | duration                                                                 | Spécifie la durée maximale pendant laquelle la tâche peut être démarrée par le déclencheur.<br/>                                   |
| [**Répétition (triggerBaseType)**](taskschedulerschema-repetition-triggerbasetype-element.md)                 | [**repetitionType**](taskschedulerschema-repetitiontype-complextype.md) | Spécifie la fréquence d’exécution de la tâche et la durée de répétition du modèle de répétition après le démarrage de la tâche.<br/>          |
| [**StartBoundary (triggerBaseType)**](taskschedulerschema-startboundary-triggerbasetype-element.md)           | dateTime                                                                 | Spécifie la date et l’heure d’activation du déclencheur.<br/>                                                              |



## <a name="attributes"></a>Attributs



| Nom | Type       | Description                               |
|------|------------|-------------------------------------------|
| Id   | **string** | Identificateur du déclencheur.<br/> |



## <a name="remarks"></a>Notes

Pour le développement de scripts, un déclencheur de démarrage est défini par l’objet [**BootTrigger**](boottrigger.md) .

Pour le développement C++, un déclencheur de démarrage est défini par l’objet [**IBootTrigger**](/windows/desktop/api/taskschd/nn-taskschd-iboottrigger) .

## <a name="examples"></a>Exemples

Pour obtenir un exemple complet du code XML d’une tâche qui spécifie un déclencheur de démarrage, consultez [exemple de déclencheur de démarrage (XML)](boot-trigger-example--xml-.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Éléments de schéma Planificateur de tâches](task-scheduler-schema-elements.md)
</dt> <dt>

[Planificateur de tâches](task-scheduler-start-page.md)
</dt> </dl>

 

 





