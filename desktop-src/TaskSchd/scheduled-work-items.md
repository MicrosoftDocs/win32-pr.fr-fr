---
title: Éléments de travail planifiés
description: Le Planificateur de tâches utilise deux termes pour décrire ce qu’il peut planifier des tâches et des éléments de travail.
ms.assetid: 6ca182c3-eba8-43dd-bf2e-27dd972e3cf8
keywords:
- éléments de travail Planificateur de tâches
- éléments de travail Planificateur de tâches, comparés aux tâches
- tâches Planificateur de tâches
- tâches Planificateur de tâches, comparées aux éléments de travail
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d19455b6d1402439403629aa5f6fca81621571fc90d9e6d8b204e741c5129414
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120080429"
---
# <a name="scheduled-work-items"></a>Éléments de travail planifiés

Le Planificateur de tâches utilise deux termes pour décrire ce qu’il peut planifier : les éléments de travail et les tâches. Parmi ces deux termes, l' [*élément de travail*](w.md) est un terme plus général qui décrit tout type d’élément pouvant être planifié. Un *élément de travail* peut être n’importe quel élément que le service Planificateur de tâches exécute à une heure spécifiée par le ou les déclencheurs de l’élément.

En revanche, une [*tâche*](t.md) est un type spécifique d’élément de travail. Actuellement, le seul type d’élément de travail planifié pris en charge est une tâche.

L’interface [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) contient des méthodes prises en charge par tous les types d’éléments de travail planifiés. Par exemple, les informations de compte, les durées d’exécution et les commentaires définis par l’application sont des propriétés qui peuvent s’appliquer à tous les types d’éléments de travail. Ces propriétés peuvent être définies et récupérées par le biais de l’interface **IScheduledWorkItem** .

L’interface [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) contient des méthodes prises en charge uniquement par les tâches.

Les méthodes de l’interface [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) sont actuellement héritées par l’interface [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) et seront à l’avenir héritées par d’autres interfaces d’élément de travail.

| Pour obtenir des exemples de                                              | Consultez                                                                                        |
|--------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| Création d’une nouvelle tâche.                                         | [Exemple de création d’une tâche à l’aide de NewWorkItem](creating-a-task-using-newworkitem-example.md) |
| Exécution d’une tâche existante.                                    | [Exemple de démarrage d’une tâche](starting-a-task-example.md)                                     |
| Récupération des propriétés qui s’appliquent à tous les types d’éléments de travail. | [Récupération d’exemples de propriétés d’élément de travail](retrieving-work-item-property-examples.md)       |
| Définition des propriétés qui s’appliquent à tous les types d’éléments de travail.    | [Définition d’exemples de propriétés d’élément de travail](setting-work-item-property-examples.md)             |



 

 

 




