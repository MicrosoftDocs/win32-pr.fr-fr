---
title: Ajouter des éléments de travail
description: Il existe deux façons d’ajouter des éléments de travail aux Tasksfolder planifiés. Vous pouvez créer un nouvel élément de travail dans le dossier, ou vous pouvez ajouter un élément de travail existant au dossier.
ms.assetid: fad5e813-a2e9-40af-97a9-4f92debf1808
keywords:
- éléments de travail Planificateur de tâches, ajouter
- tâches Planificateur de tâches, ajout
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 722f776fd36933995cfd9b5a85612b52dae63f7b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106527137"
---
# <a name="adding-work-items"></a>Ajouter des éléments de travail

Il existe deux façons d’ajouter des [*éléments de travail*](w.md) aux [*Tasksfolder planifiés*](s.md). Vous pouvez créer un nouvel élément de travail dans le dossier, ou vous pouvez ajouter un élément de travail existant au dossier.

> [!Note]  
> Actuellement, seuls les objets de tâche peuvent être ajoutés au dossier tâches planifiées. Lorsque vous ajoutez une tâche, vous devez connaître les identificateurs de la classe de tâche et de l’interface de tâche [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask).

 

Pour créer des éléments de travail, vous devez appeler la méthode [**ITaskScheduler :: NewWorkItem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-newworkitem) . Cette méthode crée un objet d’élément de travail à l’aide du nom que vous fournissez et ajoute l’élément de travail au dossier tâches planifiées. Lorsque vous créez un élément de travail, le Planificateur de tâches alloue la mémoire requise pour le nouvel objet.

Pour ajouter des éléments de travail existants au dossier tâches planifiées, appelez la méthode [**ITaskScheduler :: AddWorkItem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-addworkitem) . Lorsque vous appelez cette méthode, vous devez créer l’objet.

Les noms que vous fournissez pour les éléments de travail doivent être uniques dans le dossier tâches planifiées. Si un élément de travail du même nom existe déjà lorsque vous appelez la méthode [**ITaskScheduler :: NewWorkItem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-newworkitem) ou la méthode [**ITaskScheduler :: AddWorkItem**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-addworkitem) , la méthode retourne une erreur indiquant que le **fichier d’erreur \_ \_ existe** . Pour plus d’informations, consultez [création d’une tâche à l’aide de l’exemple NewWorkItem](creating-a-task-using-newworkitem-example.md).

 

 




