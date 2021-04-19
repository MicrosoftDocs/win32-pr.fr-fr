---
title: Exemple de démarrage d’une tâche
description: Pour démarrer une tâche, appelez la méthode Run de l’interface ITask. Run est une méthode asynchrone qui tente d’exécuter la tâche et retourne dès que la tâche a démarré. Le service de Planificateur de tâches doit être en cours d’exécution pour que cette méthode aboutisse.
ms.assetid: 90f197de-7a32-4e4b-b4c0-d3f706e47de1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 325d8d990367a810351ec4eea8b03b7dc0240cd5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106545745"
---
# <a name="starting-a-task-example"></a>Exemple de démarrage d’une tâche

Pour démarrer une tâche, appelez la méthode [**Run**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-run) de l’interface [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) . **Run** est une méthode asynchrone qui tente d’exécuter la tâche et retourne dès que la tâche a démarré. Le service de Planificateur de tâches doit être en cours d’exécution pour que cette méthode aboutisse.

La procédure suivante décrit comment démarrer une tâche.

**Pour démarrer une tâche**

1.  Appelez [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) pour initialiser la bibliothèque com et [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) pour obtenir un objet planificateur de tâches. (Cet exemple suppose que le service Planificateur de tâches est en cours d’exécution.)
2.  Appelez [**ITaskScheduler :: Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) pour récupérer l’interface [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) de l’objet Task. (Notez que cet exemple obtient la tâche « tester la tâche ».)
3.  Appelez [**Run**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-run) pour démarrer la tâche. Notez que cette méthode est héritée par l’interface [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) .
4.  Poursuivez le traitement en fonction des besoins.
5.  Appelez **ITask :: Release** pour libérer des ressources et [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) pour annuler l’initialisation de com. Cet exemple appelle [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) pour libérer le pointeur vers l’interface [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) . (Notez que **Release** est une méthode [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) héritée par **ITask**.)



| Pour obtenir un exemple de code de    | Consultez                                                                         |
|--------------------------|-----------------------------------------------------------------------------|
| Exécution d’une tâche existante | [Exemple de code C/C++ : démarrage d’une tâche](c-c-code-example-starting-a-task.md) |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Exemples de Planificateur de tâches 1,0](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 