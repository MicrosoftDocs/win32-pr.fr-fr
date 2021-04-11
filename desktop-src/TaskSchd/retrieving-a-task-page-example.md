---
title: Exemple de récupération d’une page de tâche
description: Pour récupérer une page de tâche, vous devez appeler ITask QueryInterface pour récupérer l’interface IProvideTaskPage, puis appeler IProvideTaskPage GetPage. La méthode GetPage retourne un handle vers la page, qui peut ensuite être utilisé pour afficher la page que vous avez demandée.
ms.assetid: 97525419-c480-465a-97c6-e701043c0af2
keywords:
- récupération de la page de tâches Planificateur de tâches
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd570edf3309b9b9ff0eada291d02a10850885ae
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031407"
---
# <a name="retrieving-a-task-page-example"></a>Exemple de récupération d’une page de tâche

Pour récupérer une page de tâche, vous devez appeler **ITask :: QueryInterface** pour récupérer l’interface [**IProvideTaskPage**](/windows/desktop/api/Mstask/nn-mstask-iprovidetaskpage) , puis appeler [**IProvideTaskPage :: GetPage**](/windows/desktop/api/Mstask/nf-mstask-iprovidetaskpage-getpage). La méthode **GetPage** retourne un handle vers la page, qui peut ensuite être utilisé pour afficher la page que vous avez demandée.

> [!Note]  
> Dans l’exemple de code suivant, toutes les interfaces sont libérées après qu’elles ne sont plus nécessaires.

 

La procédure suivante décrit comment créer un nouveau déclencheur.

**Pour créer un déclencheur**

1.  Appelez [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) pour initialiser la bibliothèque com et [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) pour obtenir un objet planificateur de tâches. (Cet exemple suppose que le service Planificateur de tâches est en cours d’exécution.)
2.  Appelez [**ITaskScheduler :: Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) pour récupérer l’interface [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) de l’objet Task. (Notez que cet exemple obtient la tâche « tester la tâche ».)
3.  Appelez **ITask :: QueryInterface** pour récupérer l’interface [**IProvideTaskPage**](/windows/desktop/api/Mstask/nn-mstask-iprovidetaskpage) et [**IProvideTaskPage :: GetPage**](/windows/desktop/api/Mstask/nf-mstask-iprovidetaskpage-getpage) pour récupérer la page.
4.  À l’aide du handle de page retourné, affichez la page.



| Pour obtenir un exemple de code de                                   | Consultez                                                                   |
|---------------------------------------------------------|-----------------------------------------------------------------------|
| Récupération et affichage de la page de tâche d’une tâche connue | [Récupération d’une page de tâche](c-c-code-example-retrieving-a-task-page.md) |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Exemples de Planificateur de tâches 1,0](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 