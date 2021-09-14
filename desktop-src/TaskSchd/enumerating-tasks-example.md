---
title: Exemple d’énumération de tâches
description: Pour énumérer des tâches, vous devez appeler l’énumération ITaskScheduler pour créer un objet d’énumération. Ensuite, utilisez l’interface IEnumWorkItems de l’objet d’énumération pour énumérer les tâches dans le dossier tâches planifiées.
ms.assetid: 65a8a8af-f4d8-4948-8dd4-b592f1381bfe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd929ebd7d8e9f1a3c372ce212d63dcb29df82b7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127008666"
---
# <a name="enumerating-tasks-example"></a>Exemple d’énumération de tâches

Pour énumérer des tâches, vous devez appeler [**ITaskScheduler :: enum**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-enum) pour créer un [*objet d’énumération*](e.md). Ensuite, utilisez l’interface [**IEnumWorkItems**](/windows/desktop/api/Mstask/nn-mstask-ienumworkitems) de l’objet d’énumération pour énumérer les tâches dans le dossier tâches planifiées.

La procédure suivante décrit comment énumérer les tâches dans le dossier tâches planifiées.

**Pour énumérer les tâches du dossier tâches planifiées**

1.  Appelez [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) pour initialiser la bibliothèque com et [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) pour obtenir un objet planificateur de tâches. (Cet exemple suppose que le service Planificateur de tâches est en cours d’exécution.)
2.  Appelez [**ITaskScheduler :: enum**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-enum) pour récupérer un objet d’énumération.
3.  Appelez [**IEnumWorkItems :: Next**](/windows/desktop/api/Mstask/nf-mstask-ienumworkitems-next) pour récupérer les tâches. (Cet exemple essaie de récupérer cinq tâches avec chaque appel.)
4.  Traitez les tâches retournées. (Cet exemple affiche simplement le nom de chaque tâche à l’écran.
5.  Libérer les ressources. Appelez [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) pour libérer la mémoire utilisée pour les noms.



| Pour obtenir un exemple de code de                                                         | Consultez                                                                             |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| Énumération de toutes les tâches dans le dossier tâches planifiées de l’ordinateur local | [Exemple de code C/C++ : énumération de tâches](c-c-code-example-enumerating-tasks.md) |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Exemples de Planificateur de tâches 1,0](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 