---
title: Objet ActionCollection
description: Objet de script qui contient les actions effectuées par la tâche.
ms.assetid: e887680d-e7e8-4bea-8f00-fb7645d79e60
keywords:
- actions Planificateur de tâches, objet collection
- Objet ActionCollection Planificateur de tâches
- Planificateur de tâches d’objets ActionCollection, Description
topic_type:
- apiref
api_name:
- ActionCollection
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89dee7182cc79684dec1fd052f7ad67409ba513f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519145"
---
# <a name="actioncollection-object"></a>Objet ActionCollection

Objet de script qui contient les actions effectuées par la tâche.

## <a name="members"></a>Membres

L’objet **ActionCollection** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

L’objet **ActionCollection** a ces méthodes.



| Méthode                                    | Description                                                 |
|:------------------------------------------|:------------------------------------------------------------|
| [**Effacé**](actioncollection-clear.md)   | Efface toutes les actions de la collection.<br/>      |
| [**Créés**](actioncollection-create.md) | Crée et ajoute une nouvelle action à la collection.<br/> |
| [**Installez**](actioncollection-remove.md) | Supprime une action spécifiée de la collection.<br/>  |



 

### <a name="properties"></a>Propriétés

L’objet **ActionCollection** a ces propriétés.



| Propriété                                               | Type d’accès           | Description                                                           |
|:-------------------------------------------------------|:----------------------|:----------------------------------------------------------------------|
| [**Context**](actioncollection-context.md)<br/> | Lecture/écriture<br/> | Obtient ou définit l’identificateur du principal pour la tâche.<br/> |
| [**Saut**](actioncollection-count.md)<br/>     | Lecture seule<br/>  | Obtient le nombre d’actions dans la collection.<br/>              |
| [**Élément**](actioncollection-item.md)<br/>       | Lecture seule<br/>  | Obtient une action spécifiée de la collection.<br/>               |
| [**XmlText**](actioncollection-xmltext.md)<br/> | Lecture/écriture<br/> | Obtient ou définit une version au format XML de la collection.<br/>   |



 

## <a name="remarks"></a>Notes

Lors de la lecture ou de l’écriture de données XML, les actions d’une tâche sont spécifiées dans l’élément [**actions**](taskschedulerschema-actions-tasktype-element.md) du schéma planificateur de tâches.

## <a name="examples"></a>Exemples

Pour plus d’informations et pour obtenir un exemple de code pour cet objet de script, consultez [exemple de déclenchement temporel (script)](time-trigger-example--scripting-.md), [exemple de déclenchement d’événements (script)](https://www.bing.com/search?q=Event+Trigger+Example+(Scripting)), exemple de [déclencheur quotidien (script)](daily-trigger-example--scripting-.md), [exemple de déclencheur d’inscription (](registration-trigger-example--scripting-.md)script), exemple de [déclencheur hebdomadaire (](weekly-trigger-example--scripting-.md)script), exemple de [déclencheur LOGON (script)](logon-trigger-example--scripting-.md)ou [exemple de déclencheur de démarrage](boot-trigger-example--scripting-.md)

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                    |
| Bibliothèque de types<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





