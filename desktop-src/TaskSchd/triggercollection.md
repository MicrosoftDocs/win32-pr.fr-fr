---
title: Objet TriggerCollection (Windows. UI. Xaml. h)
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
ms.openlocfilehash: 29f7288d8db0b56fc9cc8b3de7ace8c10c13959a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103273"
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
| [**Effacé**](triggercollection-clear.md)   | Efface tous les déclencheurs de la collection.<br/>                                        |
| [**Créés**](triggercollection-create.md) | Crée un déclencheur pour la tâche.<br/>                                             |
| [**Installez**](triggercollection-remove.md) | Supprime le déclencheur spécifié de la collection de déclencheurs utilisée par la tâche.<br/> |



 

### <a name="properties"></a>Propriétés

L’objet **TriggerCollection** a ces propriétés.



| Propriété                                            | Type d’accès          | Description                                                |
|:----------------------------------------------------|:---------------------|:-----------------------------------------------------------|
| [**Saut**](triggercollection-count.md)<br/> | Lecture seule<br/> | Obtient le nombre de déclencheurs dans la collection.<br/>  |
| [**Élément**](triggercollection-item.md)<br/>   | Lecture seule<br/> | Obtient le déclencheur spécifié à partir de la collection.<br/> |



 

## <a name="remarks"></a>Notes

Lors de la lecture ou de l’écriture de données XML pour une tâche, les déclencheurs de la tâche sont spécifiés dans l’élément [**triggers**](taskschedulerschema-triggers-tasktype-element.md) du schéma planificateur de tâches.

Pour plus d’informations sur chaque type de déclencheur, consultez [types de déclencheurs](trigger-types.md).

## <a name="examples"></a>Exemples

Pour plus d’informations et pour obtenir un exemple de code pour cet objet de script, consultez [exemple de déclenchement temporel (script)](time-trigger-example--scripting-.md).

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
</dt> </dl>

 

 





