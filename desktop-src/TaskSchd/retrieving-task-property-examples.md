---
title: Récupération d’exemples de propriétés de tâche
description: Pour récupérer les propriétés d’une tâche, appelez ITaskScheduler Activate pour récupérer l’interface de l’objet de tâche, puis appelez la méthode ITask appropriée pour récupérer la propriété de tâche qui vous intéresse.
ms.assetid: 9ec9d836-c735-4a32-96b1-3dbd0a31b22a
keywords:
- récupération des propriétés de la tâche Planificateur de tâches
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0e46554c32d9d30941fd837b91e80e8e20d915b0f1c68a665fd72c8f1624c8f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002387"
---
# <a name="retrieving-task-property-examples"></a>Récupération d’exemples de propriétés de tâche

Pour récupérer les propriétés d’une tâche, appelez [**ITaskScheduler :: Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) pour obtenir la récupération de l’interface de l’objet de tâche, puis appelez la méthode [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) appropriée pour récupérer la propriété de tâche qui vous intéresse. Les exemples de code figurant en bas de la page montrent comment récupérer les différentes propriétés des tâches.

Les exemples de code répertoriés en bas de la page montrent comment récupérer les propriétés qui sont propres aux objets de tâche. Pour les autres propriétés d' [*élément de travail*](w.md) qui s’appliquent également aux tâches, consultez récupération d’exemples d' [éléments de travail](retrieving-work-item-property-examples.md).

> [!Note]  
> Dans l’exemple de code suivant, toutes les interfaces sont libérées après qu’elles ne sont plus nécessaires.

 

Notez que si vous récupérez une propriété de type chaîne (par exemple, le nom de l’application, les paramètres ou le répertoire de travail), vous devez appeler [CoTaskMemFree](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) pour libérer la mémoire allouée pour la chaîne retournée.

La procédure suivante décrit comment récupérer une propriété de tâche.

**Pour récupérer une propriété de tâche**

1.  Appelez [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) pour initialiser la bibliothèque com et [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) pour obtenir un objet planificateur de tâches. (Ces exemples supposent que le service Planificateur de tâches est en cours d’exécution.)
2.  Appelez [**ITaskScheduler :: Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) pour récupérer l’interface [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) de l’objet Task. (Notez que cet exemple obtient la tâche « tester la tâche ».)
3.  Appelez la méthode [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) appropriée pour récupérer la propriété qui vous intéresse.
4.  Traitez la propriété en fonction des besoins. (Ces exemples impriment la propriété à l’écran.)
5.  Si la propriété retournée est une chaîne, appelez [CoTaskMemFree](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) pour libérer la mémoire allouée à la chaîne retournée.



| Pour obtenir un exemple de code de                                                                                                                           | Consultez                                                                                                                     |
|-------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| Récupération du nom de l’application associée à une tâche donnée                                                                             | [Exemple de code C/C++ : récupération du nom de l’application de tâche](c-c-code-example-retrieving-the-task-application-name.md)   |
| Récupération de la durée maximale pendant laquelle la tâche peut s’exécuter et afficher ce nombre à l’écran                                                 | [Exemple de code C/C++ : récupération de la tâche durée maximale](c-c-code-example-retrieving-the-task-maxruntime.md)               |
| Récupération de la chaîne de paramètre qui est exécutée lorsque la tâche est exécutée et affiche cette chaîne à l’écran                                  | [Exemple de code C/C++ : récupération des paramètres de tâche](c-c-code-example-retrieving-task-parameters.md)                       |
| Récupération du [*niveau de priorité*](p.md) de la tâche                                                                    | [Exemple de code C/C++ : récupération de la priorité d’une tâche](c-c-code-example-retrieving-task-priority.md)                           |
| Récupération du [*Répertoire de travail*](w.md) d’une tâche et affichage du chemin d’accès au répertoire de travail à l’écran | [Exemple de code C/C++ : récupération du répertoire de travail des tâches](c-c-code-example-retrieving-the-task-working-directory.md) |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Exemples de Planificateur de tâches 1,0](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 