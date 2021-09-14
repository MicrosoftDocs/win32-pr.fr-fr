---
title: Objet Trigger
description: Objet de script qui fournit les propriétés communes qui sont héritées par tous les objets déclencheurs.
ms.assetid: dfc4cb36-8bdb-4aec-963e-5f1ec1ff85aa
keywords:
- déclencheurs Planificateur de tâches, objet déclencheur
- Objet Trigger Planificateur de tâches
- Planificateur de tâches de l’objet de déclencheur, décrit
topic_type:
- apiref
api_name:
- Trigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f4a7edc6eff0bb04c81ba3bff3bb86ec0455b25
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126857236"
---
# <a name="trigger-object"></a>Objet Trigger

Objet de script qui fournit les propriétés communes qui sont héritées par tous les objets déclencheurs.

## <a name="members"></a>Membres

L’objet **déclencheur** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

L’objet **déclencheur** a ces propriétés.



| Propriété                                                            | Type d’accès           | Description                                                                                                                                         |
|:--------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**activé**](trigger-enabled.md)<br/>                       | Lecture/écriture<br/> | Obtient ou définit une valeur booléenne qui indique si le déclencheur est activé.<br/>                                                              |
| [**EndBoundary**](trigger-endboundary.md)<br/>               | Lecture/écriture<br/> | Obtient ou définit la date et l’heure de désactivation du déclencheur. Le déclencheur ne peut pas démarrer la tâche une fois qu’elle est désactivée.<br/>               |
| [**ExecutionTimeLimit**](trigger-executiontimelimit.md)<br/> | Lecture/écriture<br/> | Obtient ou définit la durée maximale pendant laquelle la tâche lancée par le déclencheur est autorisée à s’exécuter.<br/>                                         |
| [**Identifi**](trigger-id.md)<br/>                                 | Lecture/écriture<br/> | Obtient ou définit l’identificateur pour le déclencheur.<br/>                                                                                             |
| [**Répétition**](trigger-repetition.md)<br/>                 | Lecture/écriture<br/> | Obtient ou définit une valeur qui indique la fréquence d’exécution de la tâche et la durée de répétition du modèle de répétition après le démarrage de la tâche.<br/> |
| [**StartBoundary**](trigger-startboundary.md)<br/>           | Lecture/écriture<br/> | Obtient ou définit la date et l’heure d’activation du déclencheur. Le déclencheur peut démarrer la tâche une fois que le déclencheur est activé.<br/>             |
| [**Entrer**](trigger-type.md)<br/>                             |                       | Obtient le type du déclencheur.<br/>                                                                                                            |



 

## <a name="remarks"></a>Notes

L’Planificateur de tâches fournit les objets individuels suivants pour les différents déclencheurs qu’une tâche peut utiliser :

-   [**BootTrigger**](boottrigger.md)
-   [**DailyTrigger**](dailytrigger.md)
-   [**EventTrigger**](eventtrigger.md)
-   [**IdleTrigger**](idletrigger.md)
-   [**LogonTrigger**](logontrigger.md)
-   [**MonthlyDOWTrigger**](monthlydowtrigger.md)
-   [**MonthlyTrigger**](monthlytrigger.md)
-   [**RegistrationTrigger**](registrationtrigger.md)
-   [**TimeTrigger**](timetrigger.md)
-   [**WeeklyTrigger**](weeklytrigger.md)
-   [**SessionStateChangeTrigger**](sessionstatechangetrigger.md)

Lors de la lecture ou de l’écriture de données XML, les déclencheurs d’une tâche sont spécifiés dans l’élément [**triggers**](taskschedulerschema-triggers-tasktype-element.md) du schéma planificateur de tâches.

## <a name="examples"></a>Exemples

Pour plus d’informations et pour obtenir un exemple de code pour cet objet de script, consultez [exemple de déclenchement temporel (script)](time-trigger-example--scripting-.md).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                    |
| Bibliothèque de types<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**TriggerCollection**](triggercollection.md)
</dt> </dl>

 

 





