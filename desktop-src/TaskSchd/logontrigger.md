---
title: Objet LogonTrigger
description: Objet de script qui représente un déclencheur qui démarre une tâche lorsqu’un utilisateur ouvre une session.
ms.assetid: 1a1c10ce-4273-490a-a732-a8d39773203b
keywords:
- Planificateur de tâches de déclencheur de connexion, objet
- Objet LogonTrigger Planificateur de tâches
- Planificateur de tâches d’objets LogonTrigger, Description
topic_type:
- apiref
api_name:
- LogonTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1aed10ba9c0c792a5e4f882988ca07770c4ac568cb893b8ffac16a3a24efd8f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117760096"
---
# <a name="logontrigger-object"></a>Objet LogonTrigger

Objet de script qui représente un déclencheur qui démarre une tâche lorsqu’un utilisateur ouvre une session. Au démarrage du service Planificateur de tâches, tous les utilisateurs connectés sont énumérés et toutes les tâches inscrites avec des déclencheurs de connexion qui correspondent à l’utilisateur connecté sont exécutées.

## <a name="members"></a>Membres

L’objet **LogonTrigger** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

L’objet **LogonTrigger** a ces propriétés.



| Propriété                                                            | Type d’accès           | Description                                                                                                                                                                                               |
|:--------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Retarder**](logontrigger-delay.md)<br/>                      | Lecture/écriture<br/> | Obtient ou définit une valeur qui indique la durée entre le moment où l’utilisateur ouvre une session et le moment où le travail est démarré.<br/>                                                                              |
| [**Activé**](trigger-enabled.md)<br/>                       | Lecture/écriture<br/> | Héritée de l’objet [**déclencheur**](trigger.md) . Obtient ou définit une valeur booléenne qui indique si le déclencheur est activé.<br/>                                                              |
| [**EndBoundary**](trigger-endboundary.md)<br/>               | Lecture/écriture<br/> | Héritée de l’objet [**déclencheur**](trigger.md) . Obtient ou définit la date et l’heure de désactivation du déclencheur. Le déclencheur ne peut pas démarrer la tâche une fois qu’elle est désactivée.<br/>               |
| [**ExecutionTimeLimit**](trigger-executiontimelimit.md)<br/> | Lecture/écriture<br/> | Héritée de l’objet [**déclencheur**](trigger.md) . Obtient ou définit la durée maximale pendant laquelle la tâche lancée par le déclencheur est autorisée à s’exécuter.<br/>                                         |
| [**Identifi**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                | Lecture/écriture<br/> | Héritée de l’objet [**déclencheur**](trigger.md) . Obtient ou définit l’identificateur pour le déclencheur.<br/>                                                                                             |
| [**Répétition**](trigger-repetition.md)<br/>                 | Lecture/écriture<br/> | Héritée de l’objet [**déclencheur**](trigger.md) . Obtient ou définit une valeur qui indique la fréquence d’exécution de la tâche et la durée de répétition du modèle de répétition après le démarrage de la tâche.<br/> |
| [**StartBoundary**](trigger-startboundary.md)<br/>           | Lecture/écriture<br/> | Héritée de l’objet [**déclencheur**](trigger.md) . Obtient ou définit la date et l’heure d’activation du déclencheur.<br/>                                                                            |
| [**Type**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                            | Lecture seule<br/>  | Héritée de l’objet [**déclencheur**](trigger.md) . Obtient le type du déclencheur.<br/>                                                                                                            |
| [**IDutilisateur**](logontrigger-userid.md)<br/>                    | Lecture/écriture<br/> | Obtient ou définit l'identificateur de l'utilisateur.<br/>                                                                                                                                                       |



 

## <a name="remarks"></a>Remarques

Si vous souhaitez qu’une tâche soit déclenchée lorsqu’un membre d’un groupe se connecte à l’ordinateur plutôt qu’à un utilisateur spécifique, n’affectez pas de valeur à la propriété [**LogonTrigger. UserID**](logontrigger-userid.md) . Au lieu de cela, créez un déclencheur LOGON avec une propriété **LogonTrigger. UserID** vide et attribuez une valeur au principal pour la tâche à l’aide de la propriété [**principal. GroupId**](principal-groupid.md) .

Lors de la lecture ou de l’écriture de données XML pour une tâche, un déclencheur LOGON est spécifié à l’aide de l’élément [**LogonTrigger**](taskschedulerschema-logontrigger-triggergroup-element.md) du schéma planificateur de tâches.

## <a name="examples"></a>Exemples

Pour plus d’informations et pour obtenir un exemple de code pour cet objet de script, consultez [exemple de déclencheur de connexion (script)](logon-trigger-example--scripting-.md).

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
</dt> </dl>

 

 





