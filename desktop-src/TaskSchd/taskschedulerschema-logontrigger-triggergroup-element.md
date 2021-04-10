---
title: Élément LogonTrigger (triggerGroup)
description: Spécifie un déclencheur qui démarre une tâche lorsqu’un utilisateur ouvre une session.
ms.assetid: c3edee50-e053-4813-a1b2-bf1e7b575ff7
keywords:
- déclencheur LOGON, élément XML
- Élément LogonTrigger Planificateur de tâches
topic_type:
- apiref
api_name:
- LogonTrigger
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c89d0e593277f1c854850017412b49c22d8ac436
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317194"
---
# <a name="logontrigger-triggergroup-element"></a>Élément LogonTrigger (triggerGroup)

Spécifie un déclencheur qui démarre une tâche lorsqu’un utilisateur ouvre une session.

``` syntax
<xs:element name="LogonTrigger"
    type="logonTriggerType"
 />
```

L’élément **LogonTrigger** est défini par [**triggerGroup**](taskschedulerschema-triggergroup-group.md) .

## <a name="parent-element"></a>Élément parent



| Élément                                                           | Dérivé de                                                         | Description                                            |
|-------------------------------------------------------------------|----------------------------------------------------------------------|--------------------------------------------------------|
| [**Déclencheurs**](taskschedulerschema-triggers-tasktype-element.md) | [**triggersType**](taskschedulerschema-triggerstype-complextype.md) | Spécifie les déclencheurs qui démarrent la tâche.<br/> |



## <a name="child-elements"></a>Éléments enfants



| Élément                                                                                                        | Type                                                                     | Description                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| [**Délai (logonTriggerType)**](taskschedulerschema-delay-logontriggertype-element.md)                         | duration                                                                 | Intervalle de temps entre le moment où l’utilisateur ouvre une session et le moment où la tâche est démarrée.<br/>                                              |
| [**Activé (triggerBaseType)**](taskschedulerschema-enabled-triggerbasetype-element.md)                       | boolean                                                                  | Spécifie que le déclencheur est activé.<br/>                                                                                  |
| [**EndBoundary (triggerBaseType)**](taskschedulerschema-endboundary-triggerbasetype-element.md)               | dateTime                                                                 | Spécifie la date et l’heure de désactivation du déclencheur. Le déclencheur ne peut pas démarrer la tâche une fois qu’elle est désactivée.<br/> |
| [**ExecutionTimeLimit (triggerBaseType)**](taskschedulerschema-executiontimelimit-triggerbasetype-element.md) | duration                                                                 | Spécifie la durée maximale pendant laquelle la tâche peut être démarrée par le déclencheur.<br/>                                   |
| [**Répétition (triggerBaseType)**](taskschedulerschema-repetition-triggerbasetype-element.md)                 | [**repetitionType**](taskschedulerschema-repetitiontype-complextype.md) | Spécifie la fréquence d’exécution de la tâche et la durée de répétition du modèle de répétition après le démarrage de la tâche.<br/>          |
| [**StartBoundary (triggerBaseType)**](taskschedulerschema-startboundary-triggerbasetype-element.md)           | dateTime                                                                 | Spécifie la date et l’heure d’activation du déclencheur.<br/>                                                              |
| [**UserId (logonTriggerType)**](taskschedulerschema-userid-logontriggertype-element.md)                       | string                                                                   | Identificateur de l’utilisateur. La tâche est démarrée lorsque cet utilisateur ouvre une session sur l’ordinateur.<br/>                                      |



## <a name="remarks"></a>Notes

Pour le développement de scripts, un déclencheur LOGON est spécifié à l’aide de l’objet [**LogonTrigger**](logontrigger.md) .

Pour le développement C++, un déclencheur LOGON est spécifié à l’aide de l’interface [**ILogonTrigger**](/windows/desktop/api/taskschd/nn-taskschd-ilogontrigger) .

Les éléments enfants répertoriés ci-dessus sont définis par les types d’éléments complexes [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) et [**logonTriggerType**](taskschedulerschema-logontriggertype-complextype.md) . Ces éléments doivent être ajoutés dans l’ordre indiqué ci-dessous.

-   [**StartBoundary (triggerBaseType)**](taskschedulerschema-startboundary-triggerbasetype-element.md)
-   [**EndBoundary (triggerBaseType)**](taskschedulerschema-endboundary-triggerbasetype-element.md)
-   [**Activé (triggerBaseType)**](taskschedulerschema-enabled-triggerbasetype-element.md)
-   [**Répétition (triggerBaseType)**](taskschedulerschema-repetition-triggerbasetype-element.md)
-   [**ExecutionTimeLimit (triggerBaseType)**](taskschedulerschema-executiontimelimit-triggerbasetype-element.md)
-   [**UserId (logonTriggerType)**](taskschedulerschema-userid-logontriggertype-element.md)
-   [**Délai (logonTriggerType)**](taskschedulerschema-delay-logontriggertype-element.md)

### <a name="attributes"></a>Attributs

L’attribut indiqué ci-dessous est défini par les types d’éléments complexes [**triggerBaseType**](taskschedulerschema-triggerbasetype-complextype.md) .

-   ID : identificateur du déclencheur.

## <a name="examples"></a>Exemples

Pour obtenir un exemple complet du code XML d’une tâche qui utilise un déclencheur LOGON, consultez [exemple de déclencheur de connexion (XML)](logon-trigger-example--xml-.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Éléments de schéma Planificateur de tâches](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





