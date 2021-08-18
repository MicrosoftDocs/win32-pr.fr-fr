---
title: Définition d’exemples de propriétés d’élément de travail
description: Pour définir les propriétés d’un élément de travail, appelez ITaskScheduler Activate pour récupérer l’interface de l’objet d’élément de travail, puis appelez la méthode appropriée pour définir la propriété de tâche qui vous intéresse. Actuellement, les seuls éléments de travail valides sont les tâches.
ms.assetid: 80a158de-d312-499d-8ff0-b95e794cf169
keywords:
- définition des propriétés de l’élément de travail Planificateur de tâches
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6a29ff08c4f9129b8dc9ab749cd6db5807fd0c52449e48b64d5f3b36631fef6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119402539"
---
# <a name="setting-work-item-property-examples"></a>Définition d’exemples de propriétés d’élément de travail

Pour définir les propriétés d’un élément de travail, appelez [**ITaskScheduler :: Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) pour récupérer l’interface de l’objet d’élément de travail, puis appelez la méthode appropriée pour définir la propriété de tâche qui vous intéresse. Actuellement, les seuls éléments de travail valides sont les tâches.

Les exemples de code figurant en bas de la page montrent comment définir les propriétés qui s’appliquent à tous les éléments de travail. Pour les autres propriétés qui sont propres aux tâches, consultez [définition d’exemples de propriétés de tâche](setting-task-property-examples.md).

> [!Note]  
> Dans l’exemple de code suivant, toutes les interfaces sont libérées après qu’elles ne sont plus nécessaires.

 

Dans les exemples suivants, l’objet modifié est toujours enregistré sur le disque par un appel à [**IPersistFile :: Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save). (L’interface [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) est une interface COM standard héritée par l’objet Task.)

La procédure suivante décrit comment définir une propriété de tâche.

**Pour définir une propriété de tâche**

1.  Appelez [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) pour initialiser la bibliothèque com et [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) pour obtenir un objet planificateur de tâches. (Ces exemples supposent que le service Planificateur de tâches est en cours d’exécution.)
2.  Appelez [**ITaskScheduler :: Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) pour récupérer l’interface [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) de l’objet Task. (Notez que les tâches sont actuellement le seul type d’élément de travail valide.)
3.  Appelez la méthode [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) appropriée pour définir la propriété qui vous intéresse. Notez que les méthodes **IScheduledWorkItem** sont héritées par l’interface [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) .
4.  Appelez [**IPersistFile :: Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) pour stocker l’objet de tâche modifié sur le disque.



| Pour obtenir un exemple de code de                            | Consultez                                                                                                           |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Définition des informations de compte pour une tâche connue | [Exemple de code C/C++ : définition des informations de compte de tâche](c-c-code-example-setting-task-account-information.md) |
| Définition du commentaire d’une tâche connue              | [Exemple de code C/C++ : définition d’un commentaire de tâche](c-c-code-example-setting-task-comment.md)                         |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Exemples de Planificateur de tâches 1,0](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 