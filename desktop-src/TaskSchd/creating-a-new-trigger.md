---
title: Création d’un déclencheur
description: Pour créer un déclencheur, vous devez utiliser trois interfaces.
ms.assetid: c0f121ff-d0a5-4b6c-935c-6f47b4ea26d5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0111fe8c45fdac5618407500b2168bf09c4ec01c5d68e78342f14d6bf103ff78
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100439"
---
# <a name="creating-a-new-trigger"></a>Création d’un déclencheur

Pour créer un déclencheur, vous devez utiliser trois interfaces. [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem) fournit la méthode [**IScheduledWorkItem :: CreateTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) pour la création de l’objet déclencheur, [**ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger) fournit la méthode [**ITaskTrigger :: SetTrigger**](/windows/desktop/api/Mstask/nf-mstask-itasktrigger-settrigger) pour définir les critères pour le déclencheur, et l’interface com [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) fournit une méthode **Save** pour enregistrer le nouveau déclencheur sur le disque.

La procédure suivante décrit comment créer un nouveau déclencheur.

**Pour créer un déclencheur**

1.  Appelez [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) pour initialiser la bibliothèque com et [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) pour obtenir un objet planificateur de tâches. (Cet exemple suppose que le service Planificateur de tâches est en cours d’exécution.)
2.  Appelez [**ITaskScheduler :: Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) pour récupérer l’interface [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) de l’objet Task. (Notez que cet exemple obtient la tâche « tester la tâche ».)
3.  Appelez [**CreateTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) pour créer un objet déclencheur. (Notez que [**CreateTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) est héritée de [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem).)
4.  Définissez une structure de [**\_ déclencheur de tâche**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) . Notez que les membres wBeginDay, wBeginMonth et wBeginYear du **\_ déclencheur de tâche** doivent être définis sur un jour, un mois et une année valides respectivement.
5.  Appelez [**ITaskTrigger :: SetTrigger**](/windows/desktop/api/Mstask/nf-mstask-itasktrigger-settrigger) pour définir les critères de déclenchement.
6.  Enregistrez la tâche avec le nouveau déclencheur sur le disque à l’aide de [**IPersistFile :: Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save). (L’interface [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) est une interface COM standard prise en charge par l’interface [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) .)
7.  Appelez [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) pour libérer toutes les ressources. (Notez que **Release** est une méthode [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) héritée par [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).)



| Pour obtenir un exemple de code de                       | Consultez                                                                                         |
|---------------------------------------------|---------------------------------------------------------------------------------------------|
| Création d’un déclencheur pour une tâche existante | [Exemple de code C/C++ : création d’un déclencheur de tâche](c-c-code-example-creating-a-task-trigger.md) |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Exemples de Planificateur de tâches 1,0](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 