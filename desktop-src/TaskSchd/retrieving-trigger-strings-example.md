---
title: Exemple de récupération de chaînes de déclencheur
description: Vous pouvez récupérer les chaînes de déclenchement d’un déclencheur connu à l’aide de l’interface IScheduledWorkItem ou ITaskTrigger, selon le type d’objet que vous utilisez.
ms.assetid: adfa95b1-54f0-4bcd-a260-ca76fd77d43e
keywords:
- récupération des chaînes de déclencheur Planificateur de tâches
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f44708fdbb4025f5d99409297dda65504a909aec
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106511700"
---
# <a name="retrieving-trigger-strings-example"></a>Exemple de récupération de chaînes de déclencheur

Vous pouvez récupérer les chaînes de déclenchement d’un déclencheur connu à l’aide de l’interface [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) ou [**ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger) , selon le type d’objet que vous utilisez.

Lors de l’utilisation d’un [*objet Task*](t.md), utilisez les méthodes de l’interface [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) pour récupérer les chaînes de déclenchement d’un élément de travail.

Lorsque vous travaillez avec un [*objet déclencheur de tâche*](t.md), utilisez les méthodes de l’interface [**ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger) pour récupérer la chaîne de déclenchement du déclencheur.

L’exemple suivant montre comment utiliser [**IScheduledWorkItem :: GetTriggerString**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-gettriggerstring) pour afficher les chaînes de tous les déclencheurs associés à une tâche connue.

La procédure suivante décrit comment récupérer les chaînes de déclenchement d’une tâche.

**Pour récupérer les chaînes de déclenchement d’une tâche**

1.  Appelez [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) pour initialiser la bibliothèque com et [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) pour obtenir un objet planificateur de tâches. (Cet exemple suppose que le service Planificateur de tâches est en cours d’exécution.)
2.  Appelez [**ITaskScheduler :: Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) pour récupérer l’interface [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) de l’objet Task. (Notez que cet exemple obtient la tâche « tester la tâche ».)
3.  Appelez **ITask :: GetTriggerCount** pour connaître le nombre de déclencheurs associés à une tâche. (Notez que [**GetTriggerCount**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-gettriggercount) est une méthode [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) héritée par [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).)
4.  Affichez les chaînes de déclenchement, en appelant **ITask :: GetTriggerString** pour chaque déclencheur associé à la tâche. (Notez que [**GetTriggerString**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-gettriggerstring) est une méthode [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) héritée par [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).)
5.  Libérer toutes les ressources. Appelez [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) pour libérer les chaînes de déclenchement et **ITask :: Release** pour libérer l’interface [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) . (Notez que [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) est une méthode [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) héritée par **ITask**.)



| Pour obtenir un exemple de code de                                                         | Consultez                                                                                         |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| Récupération d’une chaîne de déclenchement pour tous les déclencheurs associés à une tâche connue | [Exemple de code : récupération de chaînes de déclencheur](c-c-code-example-retrieving-trigger-strings.md) |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Exemples de Planificateur de tâches 1,0](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 