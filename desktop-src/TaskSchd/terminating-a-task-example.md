---
title: Exemple de fin d’une tâche
description: Vous pouvez arrêter une tâche pendant qu’elle s’exécute en appelant IScheduledWorkItem Terminate.
ms.assetid: f8401650-e196-4959-8f23-3d649a55f73d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73e632b00a9e957849a5735d31018e3444113190
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104199315"
---
# <a name="terminating-a-task-example"></a>Exemple de fin d’une tâche

Vous pouvez arrêter une tâche pendant qu’elle s’exécute en appelant [**IScheduledWorkItem :: Terminate**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-terminate).

La procédure suivante décrit comment arrêter une tâche si elle est en cours d’exécution.

**Pour arrêter une tâche si elle est en cours d’exécution**

1.  Appelez [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) pour initialiser la bibliothèque com et [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) pour obtenir un objet planificateur de tâches. (Cet exemple suppose que le service Planificateur de tâches est en cours d’exécution.)
2.  Appelez [**ITaskScheduler :: Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) pour récupérer l’interface [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) de l’objet Task. (Notez que cet exemple obtient la tâche « tester la tâche ».)
3.  Appelez **ITask :: GetStatus** pour déterminer si la tâche est en cours d’exécution. (Notez que [**GetStatus**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-getstatus) est une méthode [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) héritée par [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).)
4.  Vérifiez l’état de la tâche, puis appelez **ITask :: Terminate** si la tâche est en cours d’exécution. (Notez que [**Terminate**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-terminate) est une méthode [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) héritée par [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).)



| Pour obtenir un exemple de code de                | Consultez                                                                               |
|--------------------------------------|-----------------------------------------------------------------------------------|
| Vérification de l’état d’une tâche connue | [Exemple de code C/C++ : fin d’une tâche](c-c-code-example-terminating-a-task.md) |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Exemples de Planificateur de tâches 1,0](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 