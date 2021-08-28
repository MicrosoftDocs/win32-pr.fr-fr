---
title: Modification d’un élément de travail à l’aide des pages de propriétés
description: Vous pouvez modifier les propriétés d’un élément de travail à l’aide de l’interface graphique utilisateur fournie par le service Planificateur de tâches.
ms.assetid: 2d7992ce-fa70-41cc-a8e7-74687171537f
keywords:
- modification des éléments de travail Planificateur de tâches
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0121a9e3100922ecdd1d529aa81b498d377724959abb5c3380337df82817e338
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100429"
---
# <a name="editing-a-work-item-using-property-pages"></a>Modification d’un élément de travail à l’aide des pages de propriétés

Vous pouvez modifier les propriétés d’un élément de travail à l’aide de l’interface graphique utilisateur fournie par le service Planificateur de tâches. (Actuellement, les seuls éléments de travail valides sont les tâches.)

La procédure suivante décrit comment modifier une tâche à l’aide de ses pages de propriétés.

**Pour modifier une tâche à l’aide de ses pages de propriétés**

1.  Appelez [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize) pour initialiser la bibliothèque com et [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) pour obtenir un objet planificateur de tâches. (Ces exemples supposent que le service Planificateur de tâches est en cours d’exécution.)
2.  Appelez [**ITaskScheduler :: Activate**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-activate) pour récupérer l’interface [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) de l’objet Task. (Notez que les tâches sont actuellement le seul type d’élément de travail valide.)
3.  Appelez [**IScheduledWorkItem :: EditWorkItem**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-editworkitem) pour afficher les pages de propriétés de la tâche.
4.  Modifiez les propriétés de la tâche en fonction des besoins, puis cliquez sur OK pour accepter les nouvelles valeurs et supprimer les pages de propriétés affichées.



| Pour obtenir un exemple de code de                                                                                      | Consultez                                                                                 |
|------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| Affichage des pages de propriétés d’une tâche connue et autorisation à un utilisateur de modifier les propriétés de l’élément de travail | [Exemple de code C/C++ : modification d’un élément de travail](c-c-code-example-editing-a-work-item.md) |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Exemples de Planificateur de tâches 1,0](task-scheduler-1-0-examples.md)
</dt> </dl>

 

 