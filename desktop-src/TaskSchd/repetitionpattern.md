---
title: Objet RepetitionPattern
description: Objet de script qui définit la fréquence d’exécution de la tâche et la durée de répétition du modèle de répétition après le démarrage de la tâche.
ms.assetid: a4e63da7-78ab-46a9-9b55-8460355753cf
keywords:
- déclencheur Planificateur de tâches, objet de modèle de répétition
- modèle de répétition Planificateur de tâches, objet
- Objet RepetitionPattern Planificateur de tâches
- Planificateur de tâches d’objets RepetitionPattern, Description
topic_type:
- apiref
api_name:
- RepetitionPattern
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84b88588238c9a7e4158fe21bca8904bf6f39b51
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464814"
---
# <a name="repetitionpattern-object"></a>Objet RepetitionPattern

Objet de script qui définit la fréquence d’exécution de la tâche et la durée de répétition du modèle de répétition après le démarrage de la tâche.

## <a name="members"></a>Membres

L’objet **RepetitionPattern** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

L’objet **RepetitionPattern** a ces propriétés.



| Propriété                                                                    | Type d’accès           | Description                                                                                                                                        |
|:----------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Duration**](repetitionpattern-duration.md)<br/>                   | Lecture/écriture<br/> | Obtient ou définit la durée de répétition du modèle.<br/>                                                                                          |
| [**Défini**](repetitionpattern-interval.md)<br/>                   | Lecture/écriture<br/> | Obtient ou définit la durée entre chaque redémarrage de la tâche.<br/>                                                                       |
| [**StopAtDurationEnd**](repetitionpattern-stopatdurationend.md)<br/> | Lecture/écriture<br/> | Obtient ou définit une valeur booléenne qui indique si une instance en cours d’exécution de la tâche est arrêtée à la fin de la durée du modèle de répétition.<br/> |



 

## <a name="remarks"></a>Notes

Si vous spécifiez une durée de répétition pour une tâche, vous devez également spécifier l’intervalle de répétition.

Si vous enregistrez une tâche qui contient un déclencheur avec un intervalle de répétition égal à une minute et une durée de répétition égale à quatre minutes, la tâche est lancée cinq fois. Les cinq répétitions peuvent être définies par le modèle suivant.

1.  Une tâche commence au début de la première minute.
2.  La tâche suivante démarre à la fin de la première minute.
3.  La tâche suivante démarre à la fin de la seconde minute.
4.  La tâche suivante démarre à la fin de la troisième minute.
5.  La tâche suivante démarre à la fin de la quatrième minute.

**Windows Server 2003, Windows XP et windows 2000 :** Si vous enregistrez une tâche qui contient un déclencheur avec un intervalle de répétition égal à une minute et une durée de répétition égale à quatre minutes, la tâche est lancée quatre fois.

Lors de la lecture ou de l’écriture de données XML pour une tâche, le modèle de répétition est spécifié à l’aide de l’élément de [**répétition**](taskschedulerschema-repetition-triggerbasetype-element.md) du schéma planificateur de tâches.

## <a name="examples"></a>Exemples

Pour plus d’informations et pour obtenir un exemple de code pour cette propriété, consultez [exemple de déclencheur quotidien (script)](daily-trigger-example--scripting-.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                    |
| Bibliothèque de types<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Objets Planificateur de tâches](task-scheduler-objects.md)
</dt> <dt>

[Planificateur de tâches](task-scheduler-start-page.md)
</dt> </dl>

 

 





