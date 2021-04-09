---
title: Définition d’exemples de propriétés d’élément de travail
description: Pour définir les propriétés d’un élément de travail, appelez ITaskScheduler Activate pour récupérer l’interface de l’objet d’élément de travail, puis appelez la méthode appropriée pour définir la propriété de tâche qui vous intéresse. Actuellement, les seuls éléments de travail valides sont les tâches.
ms.assetid: 80a158de-d312-499d-8ff0-b95e794cf169
keywords:
- définition des propriétés de l’élément de travail Planificateur de tâches
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e026ea3d2b3f6677a3d229e9289ab9b201e02b94
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103941206"
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

 

 