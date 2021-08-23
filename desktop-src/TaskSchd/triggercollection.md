---
title: objet TriggerCollection (Windows. ui. xaml. h)
description: Objet de script utilisé pour ajouter, supprimer et récupérer les déclencheurs d’une tâche.
ms.assetid: 25d89451-48b6-4ed9-9abd-19d7e8bc1fea
keywords:
- déclencheurs Planificateur de tâches, objet de collection de déclencheurs
- Objet TriggerCollection Planificateur de tâches
- Planificateur de tâches d’objets TriggerCollection, Description
topic_type:
- apiref
api_name:
- TriggerCollection
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7fd103918bc3898e56a3041221c9c70c9ede9aea5df4843cd984f2502279014
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119001937"
---
# <a name="triggercollection-object"></a>Objet TriggerCollection

Objet de script utilisé pour ajouter, supprimer et récupérer les déclencheurs d’une tâche.

## <a name="members"></a>Membres

L’objet **TriggerCollection** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

L’objet **TriggerCollection** a ces méthodes.



| Méthode                                     | Description                                                                                |
|:-------------------------------------------|:-------------------------------------------------------------------------------------------|
| [**Effacer**](triggercollection-clear.md)   | Efface tous les déclencheurs de la collection.<br/>                                        |
| [**Créer**](triggercollection-create.md) | Crée un déclencheur pour la tâche.<br/>                                             |
| [**Installez**](triggercollection-remove.md) | Supprime le déclencheur spécifié de la collection de déclencheurs utilisée par la tâche.<br/> |



 

### <a name="properties"></a>Propriétés

L’objet **TriggerCollection** a ces propriétés.



| Propriété                                            | Type d’accès          | Description                                                |
|:----------------------------------------------------|:---------------------|:-----------------------------------------------------------|
| [**Count**](triggercollection-count.md)<br/> | Lecture seule<br/> | Obtient le nombre de déclencheurs dans la collection.<br/>  |
| [**Élément**](triggercollection-item.md)<br/>   | Lecture seule<br/> | Obtient le déclencheur spécifié à partir de la collection.<br/> |



 

## <a name="remarks"></a>Remarques

Lors de la lecture ou de l’écriture de données XML pour une tâche, les déclencheurs de la tâche sont spécifiés dans l’élément [**triggers**](taskschedulerschema-triggers-tasktype-element.md) du schéma planificateur de tâches.

Pour plus d’informations sur chaque type de déclencheur, consultez [types de déclencheurs](trigger-types.md).

## <a name="examples"></a>Exemples

Pour plus d’informations et pour obtenir un exemple de code pour cet objet de script, consultez [exemple de déclenchement temporel (script)](time-trigger-example--scripting-.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                               |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                         |
| En-tête<br/>                   | <dl> <dt>Windows. ui. xaml. h</dt> </dl> |
| Bibliothèque de types<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl>      |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl>      |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Déclencheur**](trigger.md)
</dt> </dl>

 

 





