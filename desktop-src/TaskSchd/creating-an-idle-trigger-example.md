---
title: Exemple de création d’un déclencheur inactif
description: Pour créer un déclencheur inactif, vous devez spécifier un déclencheur inactif lorsque vous créez le déclencheur, et vous devez définir la durée d’inactivité de la tâche. Pour plus d’informations sur les conditions d’inactivité, consultez conditions d’inactivité de la tâche.
ms.assetid: d36a621c-4011-4c3d-b6f4-b56d1f50983c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ac38eb3eb7520fde552f009a718fe188d247e3f9fef943f0f0f79ba6ea85970
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119139542"
---
# <a name="creating-an-idle-trigger-example"></a>Exemple de création d’un déclencheur inactif

Pour créer un déclencheur inactif, vous devez spécifier un déclencheur inactif lorsque vous créez le déclencheur, et vous devez définir la durée d’inactivité de la tâche. Pour plus d’informations sur les conditions d’inactivité, consultez conditions d’inactivité de la [tâche](task-idle-conditions.md).

Après avoir créé le déclencheur inactif, appelez [**IPersistFile :: Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save) pour enregistrer le nouveau déclencheur sur le disque.

La procédure suivante décrit comment créer un déclencheur inactif pour une tâche connue.

**Pour créer un déclencheur inactif pour une tâche connue**

1.  Appelez [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) pour initialiser la bibliothèque com et [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) pour obtenir un objet planificateur de tâches. (Cet exemple suppose que le service Planificateur de tâches est en cours d’exécution.)
2.  Appelez [**ITaskScheduler :: Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) pour récupérer l’interface [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) de l’objet Task. (Notez que cet exemple obtient la tâche « tester la tâche ».)
3.  Appelez [**SetIdleWait**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-setidlewait) pour définir la durée pendant laquelle le système doit rester inactif avant que le déclencheur ne se déclenche. (Notez que **SetIdleWait** est héritée de [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem).)
4.  Définissez la structure de [**\_ déclencheur de tâche**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) et appelez [**CreateTrigger**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-createtrigger) pour créer le déclencheur inactif. (Notez que **CreateTrigger** est héritée de [**IScheduledWorkItem**](/windows/desktop/api/Mstask/nn-mstask-ischeduledworkitem).)
5.  Enregistrez la tâche avec le nouveau déclencheur inactif sur le disque à l’aide de [**IPersistFile :: Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save). (L’interface [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) est une interface COM standard prise en charge par l’interface [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) .)
6.  Appelez **ITask :: Release** pour libérer toutes les ressources. (Notez que [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) est une méthode [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) héritée par [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).)



| Pour obtenir un exemple de code de                         | Consultez                                                                                           |
|-----------------------------------------------|-----------------------------------------------------------------------------------------------|
| Création d’un déclencheur inactif pour une tâche existante | [Exemple de code C/C++ : création d’un déclencheur inactif](c-c-code-example-creating-an-idle-trigger.md) |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Exemples de Planificateur de tâches 1,0](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 