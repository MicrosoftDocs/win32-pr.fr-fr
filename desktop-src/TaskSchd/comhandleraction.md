---
title: Objet ComHandlerAction
description: Objet de script qui représente une action qui déclenche un gestionnaire.
ms.assetid: 47ffe52f-b7b7-4486-a00d-6105395f23c0
keywords:
- Action du gestionnaire COM Planificateur de tâches, objet
- Objet ComHandlerAction Planificateur de tâches
- Planificateur de tâches d’objets ComHandlerAction, Description
topic_type:
- apiref
api_name:
- ComHandlerAction
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7dd803d67d292df22e651e4393880038835c862e0e81dde19e0d0a7e15fccd32
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119659679"
---
# <a name="comhandleraction-object"></a>Objet ComHandlerAction

Objet de script qui représente une action qui déclenche un gestionnaire.

## <a name="members"></a>Membres

L’objet **ComHandlerAction** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

L’objet **ComHandlerAction** a ces propriétés.



| Propriété                                               | Type d’accès           | Description                                                                                               |
|:-------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------|
| [**ClassId**](comhandleraction-classid.md)<br/> | Lecture/écriture<br/> | Obtient ou définit l’identificateur de la classe de gestionnaire.<br/>                                              |
| [**Données**](comhandleraction-data.md)<br/>       | Lecture/écriture<br/> | Obtient ou définit les données supplémentaires associées au gestionnaire.<br/>                              |
| [**Identifi**](action-id.md)<br/>                     | Lecture/écriture<br/> | Hérité de l’objet d' [**action**](action.md) . Obtient ou définit l’identificateur de l’action.<br/> |
| [**Type**](action-type.md)<br/>                 | Lecture seule<br/>  | Hérité de l’objet d' [**action**](action.md) . Obtient le type d'action.<br/>               |



 

## <a name="remarks"></a>Remarques

Les gestionnaires COM doivent implémenter l’interface [**ITaskHandler**](/windows/desktop/api/taskschd/nn-taskschd-itaskhandler) pour que le planificateur de tâches démarre et arrête le gestionnaire. En retour, le gestionnaire COM utilise les méthodes de l’objet [**TaskHandlerStatus**](/windows/desktop/api/taskschd/nn-taskschd-itaskhandlerstatus) pour communiquer l’état au planificateur de tâches.

Lors de la lecture ou [**de l’écriture**](taskschedulerschema-comhandler-actiongroup-element.md) de données XML, une action de gestionnaire com est spécifiée dans l’élément comhandler du schéma planificateur de tâches.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                    |
| Bibliothèque de types<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**TaskHandlerStatus**](/windows/desktop/api/taskschd/nn-taskschd-itaskhandlerstatus)
</dt> <dt>

[Objets Planificateur de tâches](task-scheduler-objects.md)
</dt> <dt>

[Planificateur de tâches](task-scheduler-start-page.md)
</dt> </dl>

 

 





