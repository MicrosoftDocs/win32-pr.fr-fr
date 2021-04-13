---
title: EventTrigger, objet (Windows. UI. Xaml. h)
description: Objet de script qui représente un déclencheur qui démarre une tâche lorsqu’un événement système se produit.
ms.assetid: 79cb6591-0919-441f-ad7f-4eb7cf0f9591
keywords:
- Planificateur de tâches de déclencheur d’événement, objet
- Objet EventTrigger Planificateur de tâches
- Planificateur de tâches d’objets EventTrigger, Description
topic_type:
- apiref
api_name:
- EventTrigger
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77b80bc8336c4756dfedc041aea40f79fd5f868e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509126"
---
# <a name="eventtrigger-object"></a>EventTrigger (objet)

Objet de script qui représente un déclencheur qui démarre une tâche lorsqu’un événement système se produit.

## <a name="members"></a>Membres

L’objet **EventTrigger** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

L’objet **EventTrigger** possède les propriétés suivantes.



| Propriété                                                            | Type d’accès           | Description                                                                                                                                                                                                                                                                                                                                                                              |
|:--------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Retard**](eventtrigger-delay.md)<br/>                      | Lecture/écriture<br/> | Obtient ou définit une valeur qui indique la durée écoulée entre le moment où l’événement se produit et le moment où la tâche est démarrée.<br/>                                                                                                                                                                                                                                                            |
| [**Enabled**](trigger-enabled.md)<br/>                       | Lecture/écriture<br/> | Héritée de l’objet [**déclencheur**](trigger.md) . Obtient ou définit une valeur booléenne qui indique si le déclencheur est activé.<br/>                                                                                                                                                                                                                                             |
| [**EndBoundary**](trigger-endboundary.md)<br/>               | Lecture/écriture<br/> | Héritée de l’objet [**déclencheur**](trigger.md) . Obtient ou définit la date et l’heure de désactivation du déclencheur. Le déclencheur ne peut pas démarrer la tâche une fois qu’elle est désactivée.<br/>                                                                                                                                                                                              |
| [**ExecutionTimeLimit**](trigger-executiontimelimit.md)<br/> | Lecture/écriture<br/> | Héritée de l’objet [**déclencheur**](trigger.md) . Obtient ou définit la durée maximale pendant laquelle la tâche lancée par ce déclencheur est autorisée à s’exécuter.<br/>                                                                                                                                                                                                                       |
| [**Identifi**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_id)<br/>                                | Lecture/écriture<br/> | Héritée de l’objet [**déclencheur**](trigger.md) . Obtient ou définit l’identificateur pour le déclencheur.<br/>                                                                                                                                                                                                                                                                            |
| [**Répétition**](trigger-repetition.md)<br/>                 | Lecture/écriture<br/> | Héritée de l’objet [**déclencheur**](trigger.md) . Obtient ou définit la fréquence d’exécution de la tâche et la durée de répétition du modèle de répétition après le démarrage de la tâche.<br/>                                                                                                                                                                                                       |
| [**StartBoundary**](trigger-startboundary.md)<br/>           | Lecture/écriture<br/> | Héritée de l’objet [**déclencheur**](trigger.md) . Obtient ou définit la date et l’heure d’activation du déclencheur.<br/>                                                                                                                                                                                                                                                           |
| [**Abonnement**](eventtrigger-subscription.md)<br/>        | Lecture/écriture<br/> | Obtient ou définit la chaîne de requête XPath qui identifie l’événement qui déclenche le déclencheur.<br/>                                                                                                                                                                                                                                                                                         |
| [**Entrer**](/windows/desktop/api/taskschd/nf-taskschd-itrigger-get_type)<br/>                            | Lecture seule<br/>  | Héritée de l’objet [**déclencheur**](trigger.md) . Obtient le type du déclencheur.<br/>                                                                                                                                                                                                                                                                                           |
| [**ValueQueries**](eventtrigger-valuequeries.md)<br/>        | Lecture/écriture<br/> | Obtient ou définit une collection de requêtes XPath nommées. Chaque requête de la collection est appliquée au dernier fichier XML d’événement correspondant retourné par la requête d’abonnement spécifiée dans la propriété [**subscription**](eventtrigger-subscription.md) . Le nom de la requête peut être utilisé en tant que variable dans le message d’une action [**ShowMessageAction**](showmessageaction.md) .<br/> |



 

## <a name="remarks"></a>Notes

Vous pouvez créer au maximum 500 tâches avec des abonnements aux événements. Un abonnement aux événements qui interroge un grand nombre d’événements peut être utilisé pour déclencher une tâche qui utilise la même action en réponse aux événements journalisés.

Lors de la lecture ou de l’écriture de votre propre XML pour une tâche, un déclencheur d’événement est spécifié à l’aide de l’élément [**EventTrigger**](taskschedulerschema-eventtrigger-triggergroup-element.md) du schéma planificateur de tâches.

## <a name="examples"></a>Exemples

Pour plus d’informations et pour obtenir un exemple de code pour cet objet de script, consultez [exemple de déclencheur d’événements (script)](/previous-versions//aa446887(v=vs.85)).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                               |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                         |
| En-tête<br/>                   | <dl> <dt>Windows. UI. Xaml. h</dt> </dl> |
| Bibliothèque de types<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl>      |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl>      |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Stead**](trigger.md)
</dt> <dt>

[**TriggerCollection**](triggercollection.md)
</dt> <dt>

[**TriggerCollection. Create**](triggercollection-create.md)
</dt> </dl>

 

