---
title: Définition des exemples de propriétés de tâche
description: Pour définir les propriétés d’une tâche, appelez ITaskScheduler Activate pour récupérer l’interface de l’objet de tâche, puis appelez la méthode ITask appropriée pour définir la propriété de tâche qui vous intéresse.
ms.assetid: df438bff-1ce1-4336-93ee-1e6cab1f1ddd
keywords:
- définition des propriétés de la tâche Planificateur de tâches
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: deac57ac28a16108eb886cc56cf697cd768ca7d2e351c4517728c2972be8582f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119681629"
---
# <a name="setting-task-property-examples"></a>Définition des exemples de propriétés de tâche

Pour définir les propriétés d’une tâche, appelez [**ITaskScheduler :: Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) pour récupérer l’interface de l’objet de tâche, puis appelez la méthode [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) appropriée pour définir la propriété de tâche qui vous intéresse.

Les exemples de code répertoriés en bas de la page montrent comment définir les propriétés qui sont propres aux objets de tâche. Pour les autres propriétés d' [*élément de travail*](w.md) qui s’appliquent également aux tâches, consultez Définition d’exemples de propriétés d' [élément de travail](setting-work-item-property-examples.md).

> [!Note]  
> Dans l’exemple de code suivant, toutes les interfaces sont libérées après qu’elles ne sont plus nécessaires.

 

Dans les exemples suivants, l’objet de tâche modifié est toujours enregistré sur le disque par un appel à [**IPersistFile :: Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save). (L’interface [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) est une interface COM standard héritée par l’objet Task.)

La procédure suivante décrit comment définir une propriété de tâche.

**Pour définir une propriété de tâche**

1.  Appelez [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) pour initialiser la bibliothèque com et [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) pour obtenir un objet planificateur de tâches. (Ces exemples supposent que le service Planificateur de tâches est en cours d’exécution.)
2.  Appelez [**ITaskScheduler :: Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) pour récupérer l’interface [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) de l’objet Task. (Notez que cet exemple obtient la tâche « tester la tâche ».)
3.  Appelez la méthode [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) appropriée pour définir la propriété qui vous intéresse.
4.  Appelez [**IPersistFile :: Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) pour stocker l’objet de tâche modifié sur le disque.



| Pour obtenir un exemple de code de                                                                                                                                | Consultez                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| Définition du nom de l’application associée à une tâche connue                                                                                     | [Exemple de code C/C++ : définition du nom de l’application](c-c-code-example-setting-application-name.md)   |
| Définition de la durée maximale d’exécution d’une tâche connue                                                                                                         | [Exemple de code C/C++ : définition de durée maximale](c-c-code-example-setting-maxruntime.md)               |
| Effacement de tous les paramètres de ligne de commande associés à une tâche connue                                                                                    | [Exemple de code C/C++ : définition de paramètres de tâche](c-c-code-example-setting-task-parameters.md)     |
| Cet exemple définit la priorité d’une tâche de test, puis enregistre la tâche. Cet exemple suppose que la tâche de test existe déjà sur l’ordinateur local. | [Exemple de code C/C++ : définition de la priorité de la tâche](c-c-code-example-setting-task-priority.md)         |
| Définition du [*Répertoire de travail*](w.md) d’une tâche connue                                                                  | [Exemple de code C/C++ : définition du répertoire de travail](c-c-code-example-setting-working-directory.md) |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Exemples de Planificateur de tâches 1,0](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 