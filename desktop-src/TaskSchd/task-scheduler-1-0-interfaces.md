---
title: Interfaces Planificateur de tâches 1,0
description: les interfaces décrites dans les rubriques suivantes fournissent un accès par programme aux fonctionnalités disponibles dans le Planificateur de tâches utilisé dans les systèmes d’exploitation Windows 2000, Windows XP et Windows Server 2003.
ms.assetid: 25f9c1ad-1859-4788-a876-6f4faa6e556e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60d2033c78594c0f4ef1d9f871275f425ef5189240ed7b432266464343cf86e2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119975029"
---
# <a name="task-scheduler-10-interfaces"></a>Interfaces Planificateur de tâches 1,0

\[\[Cette API peut être modifiée ou indisponible dans les versions ultérieures du système d’exploitation ou du produit. Utilisez à la place les [Interfaces Planificateur de tâches 2,0](task-scheduler-2-0-interfaces.md) ou [Planificateur de tâches 2,0](task-scheduler-2-0-enumerated-types.md) . \]\]

les interfaces décrites dans les rubriques suivantes fournissent un accès par programme aux fonctionnalités disponibles dans le Planificateur de tâches utilisé dans les systèmes d’exploitation Windows 2000, Windows XP et Windows Server 2003.

Ces rubriques contiennent une description de l’interface, une liste des propriétés et des méthodes définies par l’interface, ainsi que des remarques sur les circonstances spéciales qui doivent être notées lors de l’utilisation de l’interface.


Les interfaces suivantes sont introduites par Planificateur de tâches 1,0.



| Interface                                        | Description                                                                                                                                                                                                                           |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IEnumWorkItems**](/windows/desktop/api/Mstask/nn-mstask-ienumworkitems)         | Fournit les méthodes pour énumérer les tâches dans le [*dossier tâches planifiées*](s.md).                                                                                                              |
| [**IProvideTaskPage**](/windows/desktop/api/Mstask/nn-mstask-iprovidetaskpage)     | Fournit les méthodes pour accéder aux paramètres de la feuille de propriétés d’une tâche.                                                                                                                                                                 |
| [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) | Fournit les méthodes pour la gestion d' [*éléments de travail*](w.md)spécifiques.                                                                                                                                                 |
| [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask)                           | Fournit les méthodes permettant d’exécuter des tâches, d’obtenir ou de définir des informations sur les tâches et d’arrêter des tâches. Elle est dérivée de l’interface [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) et hérite de toutes les méthodes de cette interface. |
| [**ITaskScheduler**](/windows/desktop/api/Mstask/nn-mstask-itaskscheduler)         | Fournit les méthodes de planification des tâches.                                                                                                                                                                                            |
| [**ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger)             | Fournit les méthodes permettant d’accéder aux déclencheurs d’une tâche et de les définir. Les déclencheurs spécifient les heures de début de tâche, les critères de répétition et d’autres paramètres qui contrôlent le moment où une tâche est exécutée.                                                     |



 

 

 




