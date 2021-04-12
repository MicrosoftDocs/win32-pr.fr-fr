---
title: Récupération d’exemples de propriétés d’élément de travail
description: Pour récupérer les propriétés d’un élément de travail, appelez ITaskScheduler Activate pour récupérer l’interface de l’objet d’élément de travail, puis appelez la méthode appropriée pour récupérer la propriété de tâche qui vous intéresse.
ms.assetid: d9723dea-1a82-4993-b4d0-bc7d944e775f
keywords:
- récupération des propriétés de l’élément de travail Planificateur de tâches
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74a51c623301a4a3b53369713abe95ea1dafba80
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382230"
---
# <a name="retrieving-work-item-property-examples"></a>Récupération d’exemples de propriétés d’élément de travail

Pour récupérer les propriétés d’un élément de travail, appelez [**ITaskScheduler :: Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) pour récupérer l’interface de l’objet d’élément de travail, puis appelez la méthode appropriée pour récupérer la propriété de tâche qui vous intéresse. Actuellement, les seuls éléments de travail valides sont les tâches.

Les exemples de code listés en bas de cette page montrent comment récupérer les propriétés qui s’appliquent à tous les éléments de travail. Pour les autres propriétés qui sont propres aux tâches, consultez [définition d’exemples de propriétés de tâche](setting-task-property-examples.md).

> [!Note]  
> Dans l’exemple de code suivant, toutes les interfaces sont libérées après qu’elles ne sont plus nécessaires.

 

Notez que si vous récupérez une propriété de type chaîne (par exemple, un commentaire pour un élément de travail), vous devez appeler [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) pour libérer la mémoire allouée pour la chaîne retournée.

La procédure suivante décrit comment récupérer une propriété de tâche.

**Pour récupérer une propriété de tâche**

1.  Appelez [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) pour initialiser la bibliothèque com et [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) pour obtenir un objet planificateur de tâches. (Ces exemples supposent que le service Planificateur de tâches est en cours d’exécution.)
2.  Appelez [**ITaskScheduler :: Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) pour récupérer l’interface [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) de l’objet Task. (Notez que les tâches sont actuellement le seul type d’élément de travail valide.)
3.  Appelez la méthode appropriée pour récupérer la propriété qui vous intéresse.
4.  Traitez la propriété en fonction des besoins. (Ces exemples impriment simplement la propriété à l’écran.)
5.  Si la propriété retournée est une chaîne, appelez [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) pour libérer la mémoire allouée à la chaîne retournée.



| Pour obtenir un exemple de code de                                                                        | Consultez                                                                                                                       |
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| Récupération des informations de compte d’une tâche connue                                           | [Exemple de code C/C++ : récupération des informations de compte de tâche](c-c-code-example-retrieving-task-account-information.md)       |
| Récupération de la chaîne de commentaire d’une tâche connue                                                | [Exemple de code C/C++ : récupération d’un commentaire de tâche](c-c-code-example-retrieving-a-task-comment.md)                           |
| Récupération du nom du créateur de la tâche et affichage à l’écran               | [Exemple de code C/C++ : récupération du créateur de tâche](c-c-code-example-retrieving-the-task-creator.md)                       |
| Récupération du dernier code de sortie retourné par une tâche connue                                       | [Exemple de code C/C++ : récupération du code de sortie de la tâche](c-c-code-example-retrieving-task-exit-code.md)                           |
| Récupération du temps d’inactivité de la tâche et affichage à l’écran                    | [Exemple de code C/C++ : récupération d’une tâche inactive-temps d’attente](c-c-code-example-retrieving-task-idle-wait-time.md)                 |
| Récupération de l’heure de la dernière exécution de la tâche et affichage à l’écran                    | [Exemple de code C/C++ : récupération de la tâche MostRecentRun temps](c-c-code-example-retrieving-the-task-mostrecentrun-time.md) |
| Récupération la prochaine fois que la tâche est planifiée pour s’exécuter et afficher cette heure à l’écran | [Exemple de code C/C++ : récupération de la tâche NextRun temps](c-c-code-example-retrieving-the-task-nextrun-time.md)             |
| Récupération des durées d’exécution de la tâche et affichage de celles-ci à l’écran                       | [Exemple de code C/C++ : récupération des durées d’exécution des tâches](c-c-code-example-retrieving-task-run-times.md)                           |
| Récupération de l’état actuel de la tâche et affichage à l’écran                    | [Exemple de code C/C++ : récupération de l’état de la tâche](c-c-code-example-retrieving-task-status.md)                                 |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Exemples de Planificateur de tâches 1,0](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 