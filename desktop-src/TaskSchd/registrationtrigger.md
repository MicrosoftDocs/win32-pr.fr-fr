---
title: Objet RegistrationTrigger
description: Objet de script qui représente un déclencheur qui démarre une tâche lorsque la tâche est inscrite ou mise à jour.
ms.assetid: 430ef3e0-9409-49ff-8ffb-31833938d8b2
keywords:
- Planificateur de tâches de déclencheur d’inscription, objet
- Objet RegistrationTrigger Planificateur de tâches
- Planificateur de tâches d’objets RegistrationTrigger, Description
topic_type:
- apiref
api_name:
- RegistrationTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85020e3c5a2d5c3167ac2ec6ed251a37c1bc98056dae867a5a07b63ee7148dae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117759570"
---
# <a name="registrationtrigger-object"></a>Objet RegistrationTrigger

Objet de script qui représente un déclencheur qui démarre une tâche lorsque la tâche est inscrite ou mise à jour.

## <a name="members"></a>Membres

L’objet **RegistrationTrigger** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

L’objet **RegistrationTrigger** a ces propriétés.



| Propriété                                                            | Type d’accès           | Description                                                                                                                                                                                 |
|:--------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Retarder**](registrationtrigger-delay.md)<br/>               | Lecture/écriture<br/> | Obtient ou définit le laps de temps entre le moment où la tâche est inscrite et le moment où elle est démarrée.<br/>                                                                                |
| [**Activé**](trigger-enabled.md)<br/>                       | Lecture/écriture<br/> | Héritée de l’objet [**déclencheur**](trigger.md) . Obtient ou définit une valeur booléenne qui indique si le déclencheur est activé.<br/>                                                |
| [**EndBoundary**](trigger-endboundary.md)<br/>               | Lecture/écriture<br/> | Héritée de l’objet [**déclencheur**](trigger.md) . Obtient ou définit la date et l’heure de désactivation du déclencheur. Le déclencheur ne peut pas démarrer la tâche une fois qu’elle est désactivée.<br/> |
| [**ExecutionTimeLimit**](trigger-executiontimelimit.md)<br/> | Lecture/écriture<br/> | Héritée de l’objet [**déclencheur**](trigger.md) . Obtient ou définit la durée maximale pendant laquelle la tâche lancée par le déclencheur est autorisée à s’exécuter.<br/>                           |
| [**Identifi**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                | Lecture/écriture<br/> | Héritée de l’objet [**déclencheur**](trigger.md) . Obtient ou définit l’identificateur pour le déclencheur.<br/>                                                                               |
| [**Répétition**](trigger-repetition.md)<br/>                 | Lecture/écriture<br/> | Héritée de l’objet [**déclencheur**](trigger.md) . Obtient ou définit la fréquence d’exécution de la tâche et la durée de répétition du modèle de répétition après le démarrage de la tâche.<br/>          |
| [**StartBoundary**](trigger-startboundary.md)<br/>           | Lecture/écriture<br/> | Héritée de l’objet [**déclencheur**](trigger.md) . Obtient ou définit la date et l’heure d’activation du déclencheur.<br/>                                                              |
| [**Type**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                            | Lecture seule<br/>  | Héritée de l’objet [**déclencheur**](trigger.md) . Obtient le type du déclencheur.<br/>                                                                                              |



 

## <a name="remarks"></a>Remarques

Lors de la création de votre propre XML pour une tâche, un déclencheur d’inscription est spécifié à l’aide de l’élément [**RegistrationTrigger**](taskschedulerschema-registrationtrigger-triggergroup-element.md) du schéma planificateur de tâches.

Si une tâche avec un déclencheur d’inscription différé est inscrite et que l’ordinateur sur lequel la tâche est inscrite est arrêté ou redémarré pendant le délai, avant l’exécution de la tâche, la tâche ne s’exécutera pas et le délai sera perdu.

## <a name="examples"></a>Exemples

Pour plus d’informations et pour obtenir un exemple de code pour cet objet de script, consultez [exemple de déclencheur d’inscription (script)](registration-trigger-example--scripting-.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                    |
| Bibliothèque de types<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Déclencheur**](trigger.md)
</dt> <dt>

[**TriggerCollection**](triggercollection.md)
</dt> <dt>

[**TriggerCollection. Create**](triggercollection-create.md)
</dt> </dl>

 

 





