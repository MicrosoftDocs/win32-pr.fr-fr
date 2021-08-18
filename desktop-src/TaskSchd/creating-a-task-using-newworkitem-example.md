---
title: Exemple de création d’une tâche à l’aide de NewWorkItem
description: Lorsque vous créez une tâche, vous allez utiliser deux interfaces Planificateur de tâches ITaskScheduler et ITask.
ms.assetid: 1cbdba6a-e017-4f00-87cb-970686a69e0a
keywords:
- créer des éléments de travail Planificateur de tâches
- éléments de travail Planificateur de tâches, création de tâches
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc6d0e0d216c5aaccee6a51cbac939b2b3bfa421338e12d66ffdd3b8cf055862
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119139582"
---
# <a name="creating-a-task-using-newworkitem-example"></a>Exemple de création d’une tâche à l’aide de NewWorkItem

Lorsque vous créez une tâche, vous allez utiliser deux interfaces de Planificateur de tâches : [**ITaskScheduler**](/windows/desktop/api/Mstask/nn-mstask-itaskscheduler) et [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask). Vous devez fournir un nom unique pour la tâche, l’identificateur de classe de l’objet de tâche et l’identificateur d’interface de **ITask**. L’identificateur de classe et l’identificateur d’interface sont affichés dans l’exemple de code qui suit cette rubrique.

> [!Note]  
> Vous pouvez également créer une tâche en appelant [**ITaskScheduler :: AddWorkItem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-addworkitem). Lorsque vous prenez cet itinéraire, il vous incombe de créer une instance de l’objet de **tâche** (qui prend en charge l’interface [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) ), puis d’ajouter la tâche avec le nom que vous fournissez.

 

> [!Note]  
> par défaut, seul un membre du groupe administrateurs, opérateurs de sauvegarde ou opérateurs de serveur peut créer des tâches sur Windows Server 2003. un membre du groupe administrateurs peut modifier le descripteur de sécurité du \\ dossier de tâches Windows pour permettre à d’autres utilisateurs de créer des tâches.

 

Le nom que vous fournissez pour la tâche doit être unique dans le dossier tâches planifiées. Si une tâche portant le même nom existe déjà, [**ITaskScheduler :: NewWorkItem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-newworkitem) retourne le \_ fichier d’erreurs \_ existe. Si vous recevez cette valeur de retour, vous devez spécifier un autre nom et tenter à nouveau de créer la tâche.

La procédure suivante décrit comment créer une tâche d’élément de travail.

**Pour créer une tâche d’élément de travail**

1.  Appelez [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) pour initialiser la bibliothèque com et [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) pour obtenir un objet planificateur de tâches. (Cet exemple suppose que le service Planificateur de tâches est en cours d’exécution.)
2.  Appelez [**ITaskScheduler :: NewWorkItem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-newworkitem) pour créer une nouvelle tâche. (Cette méthode retourne un pointeur vers une interface [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) .)
3.  Enregistrez la nouvelle tâche sur le disque en appelant [**IPersistFile :: Save**](/windows/win32/api/objidl/nf-objidl-ipersistfile-save). (L’interface [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) est une interface COM standard prise en charge par l’interface **ITask** .)
4.  Appelez **ITask :: Release** pour libérer toutes les ressources. (Notez que [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) est une méthode [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) héritée par [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).)



| Pour obtenir un exemple de code de  | Consultez                                                                                                             |
|------------------------|-----------------------------------------------------------------------------------------------------------------|
| Création d’une tâche unique | [Exemple de code C/C++ : création d’une tâche à l’aide de NewWorkItem](c-c-code-example-creating-a-task-using-newworkitem.md) |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Exemples de Planificateur de tâches 1,0](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 