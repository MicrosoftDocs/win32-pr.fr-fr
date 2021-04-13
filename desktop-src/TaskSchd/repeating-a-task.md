---
title: Répétition d’une tâche
description: Planificateur de tâches pouvez exécuter une tâche autant de fois qu’un déclencheur a été déclenché.
ms.assetid: 69c60713-134c-4602-9e7b-cc3eea871068
keywords:
- modèle de répétition Planificateur de tâches
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 451b2c2cf7e48c40496ddba95728f435ab494ab7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310654"
---
# <a name="repeating-a-task"></a><span data-ttu-id="c1928-104">Répétition d’une tâche</span><span class="sxs-lookup"><span data-stu-id="c1928-104">Repeating A Task</span></span>

<span data-ttu-id="c1928-105">Planificateur de tâches pouvez exécuter une tâche autant de fois qu’un déclencheur a été déclenché.</span><span class="sxs-lookup"><span data-stu-id="c1928-105">Task Scheduler can run a task any number of times times after a trigger is fired.</span></span> <span data-ttu-id="c1928-106">Pour ce faire, le déclencheur définit un modèle de répétition qui indique Planificateur de tâches combien de temps il doit continuer à répéter la tâche et l’intervalle de temps entre chaque répétition de tâche.</span><span class="sxs-lookup"><span data-stu-id="c1928-106">To do this, the trigger defines a repetition pattern that tells Task Scheduler how long it should continue to repeat the task and the time interval between each task repetition.</span></span>

## <a name="repetition-pattern"></a><span data-ttu-id="c1928-107">Modèle de répétition</span><span class="sxs-lookup"><span data-stu-id="c1928-107">Repetition Pattern</span></span>

<span data-ttu-id="c1928-108">L’illustration suivante montre un modèle de répétition avec une durée de 60 minutes et un intervalle de 25 minutes.</span><span class="sxs-lookup"><span data-stu-id="c1928-108">The following illustration shows a repetition pattern with a duration of 60 minutes and an interval of 25 minutes.</span></span> <span data-ttu-id="c1928-109">Sachez que dans ce cas, Planificateur de tâches exécute la tâche lorsque le déclencheur est activé, il réexécute la tâche après 25 minutes, puis réexécute la tâche après 50 minutes en fonction du paramètre de la [**propriété StopAtDurationEnd de IRepetitionPattern**](/windows/desktop/api/taskschd/nf-taskschd-irepetitionpattern-get_stopatdurationend) ([**RepetitionPattern. StopAtDurationEnd**](repetitionpattern-stopatdurationend.md) pour les scripts).</span><span class="sxs-lookup"><span data-stu-id="c1928-109">Be aware that in this case, Task Scheduler runs the task when the trigger is fired, it runs the task again after 25 minutes, then runs the task again after 50 minutes depending on the setting of the [**StopAtDurationEnd property of IRepetitionPattern**](/windows/desktop/api/taskschd/nf-taskschd-irepetitionpattern-get_stopatdurationend) ([**RepetitionPattern.StopAtDurationEnd**](repetitionpattern-stopatdurationend.md) for scripting).</span></span> <span data-ttu-id="c1928-110">Si la propriété **StopAtDurationEnd** est définie sur True, planificateur de tâches arrête la dernière instance de la tâche si elle est toujours en cours d’exécution après 60 minutes.</span><span class="sxs-lookup"><span data-stu-id="c1928-110">If the **StopAtDurationEnd** property is set to True, Task Scheduler stops the last instance of the task if it is still running after 60 minutes.</span></span> <span data-ttu-id="c1928-111">Si la propriété **StopAtDurationEnd** est définie sur false, la dernière instance de la tâche est exécutée, quelle que soit la durée.</span><span class="sxs-lookup"><span data-stu-id="c1928-111">If the **StopAtDurationEnd** property is set to False, the last instance of the task is run regardless of the duration.</span></span>

![modèle de répétition de déclencheur](images/repetition-pattern.png)

<span data-ttu-id="c1928-113">Si vous enregistrez une tâche qui contient un déclencheur avec un intervalle de répétition égal à une minute et une durée de répétition égale à quatre minutes, la tâche est démarrée cinq fois.</span><span class="sxs-lookup"><span data-stu-id="c1928-113">If you register a task that contains a trigger with a repetition interval equal to one minute and a repetition duration equal to four minutes, the task will be started five times.</span></span> <span data-ttu-id="c1928-114">Les cinq répétitions peuvent être définies par le modèle suivant :</span><span class="sxs-lookup"><span data-stu-id="c1928-114">The five repetitions can be defined by the following pattern:</span></span>

1.  <span data-ttu-id="c1928-115">Une tâche commence au début de la première minute.</span><span class="sxs-lookup"><span data-stu-id="c1928-115">A task starts at the beginning of the first minute.</span></span>
2.  <span data-ttu-id="c1928-116">La tâche suivante démarre à la fin de la première minute.</span><span class="sxs-lookup"><span data-stu-id="c1928-116">The next task starts at the end of the first minute.</span></span>
3.  <span data-ttu-id="c1928-117">La tâche suivante démarre à la fin de la seconde minute.</span><span class="sxs-lookup"><span data-stu-id="c1928-117">The next task starts at the end of the second minute.</span></span>
4.  <span data-ttu-id="c1928-118">La tâche suivante démarre à la fin de la troisième minute.</span><span class="sxs-lookup"><span data-stu-id="c1928-118">The next task starts at the end of the third minute.</span></span>
5.  <span data-ttu-id="c1928-119">La tâche suivante démarre à la fin de la quatrième minute.</span><span class="sxs-lookup"><span data-stu-id="c1928-119">The next task starts at the end of the fourth minute.</span></span>

<span data-ttu-id="c1928-120">**Windows Server 2003, Windows XP et windows 2000 :** Si vous enregistrez une tâche qui contient un déclencheur avec un intervalle de répétition égal à une minute et une durée de répétition égale à quatre minutes, la tâche est démarrée quatre fois.</span><span class="sxs-lookup"><span data-stu-id="c1928-120">**Windows Server 2003, Windows XP and Windows 2000:** If you register a task that contains a trigger with a repetition interval equal to one minute and a repetition duration equal to four minutes, the task will be started four times.</span></span>

## <a name="objects-interfaces-and-xml-elements"></a><span data-ttu-id="c1928-121">Objets, interfaces et éléments XML</span><span class="sxs-lookup"><span data-stu-id="c1928-121">Objects, Interfaces, and XML Elements</span></span>

<span data-ttu-id="c1928-122">Pour le développement de scripts, le modèle de répétition est défini à l’aide de l’objet [**RepetitionPattern**](repetitionpattern.md) .</span><span class="sxs-lookup"><span data-stu-id="c1928-122">For scripting development, the repetition pattern is defined using the [**RepetitionPattern**](repetitionpattern.md) object.</span></span>

<span data-ttu-id="c1928-123">Pour le développement C++, le modèle de répétition est défini par l’interface [**IRepetitionPattern**](/windows/desktop/api/taskschd/nn-taskschd-irepetitionpattern) .</span><span class="sxs-lookup"><span data-stu-id="c1928-123">For C++ development, the repetition pattern is defined by the [**IRepetitionPattern**](/windows/desktop/api/taskschd/nn-taskschd-irepetitionpattern) interface.</span></span>

<span data-ttu-id="c1928-124">Lors de la lecture ou de l’écriture de données XML pour une tâche, le modèle de répétition est spécifié dans l’élément à [**répétition**](taskschedulerschema-repetition-triggerbasetype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="c1928-124">When reading or writing XML for a task, the repetition pattern is specified in the [**Repetition**](taskschedulerschema-repetition-triggerbasetype-element.md) element.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c1928-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c1928-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c1928-126">Déclencheurs de tâche</span><span class="sxs-lookup"><span data-stu-id="c1928-126">Task Triggers</span></span>](task-triggers.md)
</dt> </dl>

 

 




