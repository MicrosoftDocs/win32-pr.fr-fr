---
title: Manipuler des éléments de travail
description: L’interface IScheduledWorkItem fournit des méthodes pour récupérer et définir des propriétés d’élément de travail ; création, récupération et suppression de déclencheurs pour les éléments de travail (la définition du déclencheur doit être effectuée à l’aide de la méthode ITaskTrigger SetTrigger); et pour exécuter, terminer et supprimer l’élément de travail. Remarque pour les propriétés d’un type d’élément de travail spécifique, reportez-vous à l’interface de ce type d’objet. Par exemple, vous ne pouvez pas définir le niveau de priorité d’un élément de travail ; Toutefois, vous pouvez utiliser les méthodes de l’interface ITask pour récupérer et définir la priorité d’une tâche.
ms.assetid: 8aedf96d-e43d-4aac-ad8c-860379209f95
keywords:
- éléments de travail Planificateur de tâches, gestion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7aca2a904391926ae46749d72421fe20fe21932f758dc6e935883c4a2f750c5d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119517659"
---
# <a name="manipulating-work-items"></a>Manipuler des éléments de travail

L’interface [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) fournit des méthodes pour récupérer et définir des propriétés d’élément de travail ; création, récupération et suppression de déclencheurs pour les éléments de travail (la définition du déclencheur doit être effectuée à l’aide de la méthode [**ITaskTrigger :: SetTrigger**](/windows/desktop/api/Mstask/nf-mstask-itasktrigger-settrigger) ); et pour exécuter, terminer et supprimer l’élément de travail.

> [!Note]  
> Pour les propriétés d’un type d’élément de travail spécifique, reportez-vous à l’interface de ce type d’objet. Par exemple, vous ne pouvez pas définir le niveau de priorité d’un élément de travail ; Toutefois, vous pouvez utiliser les méthodes de l’interface [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) pour récupérer et définir la priorité d’une tâche.

 

Chaque fois que vous modifiez un élément de travail, vous devez appeler l’objet [**IPersistFile :: Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) pour enregistrer l’élément de travail modifié sur le disque. L’interface [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) est une interface COM standard qui est prise en charge par l’interface [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) .

| Pour obtenir des exemples de                                                            | Consultez                                                                                  |
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| Récupération des propriétés qui s’appliquent à tous les types d’éléments de travail                | [Récupération d’exemples de propriétés d’élément de travail](retrieving-work-item-property-examples.md) |
| Définition des propriétés qui s’appliquent à tous les types d’éléments de travail                   | [Définition d’exemples de propriétés d’élément de travail](setting-work-item-property-examples.md)       |
| Exécution d’une tâche connue                                                       | [Exemple de démarrage d’une tâche](starting-a-task-example.md)                               |
| Fin d’une tâche en cours d’exécution                                                 | [Exemple de fin d’une tâche](terminating-a-task-example.md)                         |
| Création d’un déclencheur pour une tâche connue                                    | [Création d’un déclencheur](creating-a-new-trigger.md)                                 |
| Création d’un déclencheur inactif basé sur des événements pour une tâche connue                      | [Exemple de création d’un déclencheur inactif](creating-an-idle-trigger-example.md)             |
| Récupération de la chaîne de déclenchement de tous les déclencheurs associés à une tâche connue | [Exemple de récupération de chaînes de déclencheur](retrieving-trigger-strings-example.md)         |



 

 

 