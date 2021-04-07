---
title: Énumération des tâches et affichage des informations sur les tâches
description: L’affichage d’informations sur une tâche, telles que le nom de la tâche, l’État ou la dernière exécution de la tâche, s’effectue en énumérant des tâches en cours d’exécution ou les tâches d’un dossier de tâches et en affichant les informations souhaitées.
ms.assetid: a0305089-89ff-42b7-b3f1-99a6484d2e5e
keywords:
- énumération des tâches Planificateur de tâches
- Exemples de Planificateur de tâches Planificateur de tâches, énumération de tâches
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58e4c1bbad0a1fa8892e38a001ff54e665f0c144
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671053"
---
# <a name="enumerating-tasks-and-displaying-task-information"></a><span data-ttu-id="c73bb-105">Énumération des tâches et affichage des informations sur les tâches</span><span class="sxs-lookup"><span data-stu-id="c73bb-105">Enumerating Tasks and Displaying Task Information</span></span>

<span data-ttu-id="c73bb-106">L’affichage d’informations sur une tâche, telles que le nom de la tâche, l’État ou la dernière exécution de la tâche, s’effectue en énumérant des tâches en cours d’exécution ou les tâches d’un dossier de tâches et en affichant les informations souhaitées.</span><span class="sxs-lookup"><span data-stu-id="c73bb-106">Displaying information about a task, such as the task name, state, or the last time the task was run, is done by enumerating through running tasks or the tasks in a task folder and displaying the desired information.</span></span>

## <a name="accessing-properties-of-registered-tasks"></a><span data-ttu-id="c73bb-107">Accès aux propriétés des tâches inscrites</span><span class="sxs-lookup"><span data-stu-id="c73bb-107">Accessing Properties of Registered Tasks</span></span>

<span data-ttu-id="c73bb-108">Pour afficher la valeur de la propriété d’une tâche inscrite, vous devez vous connecter au service Planificateur de tâches, puis obtenir une instance du dossier de tâches qui contient les tâches pour lesquelles vous souhaitez obtenir des informations.</span><span class="sxs-lookup"><span data-stu-id="c73bb-108">To display a registered task's property value, you must connect to the Task Scheduler service, and then get an instance of the task folder that contains the tasks you want information about.</span></span> <span data-ttu-id="c73bb-109">Vous pouvez ensuite obtenir une collection de toutes les tâches inscrites dans le dossier de tâches.</span><span class="sxs-lookup"><span data-stu-id="c73bb-109">You then get a collection of all the registered tasks in the task folder.</span></span> <span data-ttu-id="c73bb-110">Vous allez ensuite énumérer chaque tâche inscrite et obtenir et afficher une valeur de propriété pour chaque tâche.</span><span class="sxs-lookup"><span data-stu-id="c73bb-110">Then you enumerate through each registered task and get and display a property value for each task.</span></span>

## <a name="accessing-properties-of-running-tasks"></a><span data-ttu-id="c73bb-111">Accès aux propriétés des tâches en cours d’exécution</span><span class="sxs-lookup"><span data-stu-id="c73bb-111">Accessing Properties of Running Tasks</span></span>

<span data-ttu-id="c73bb-112">Pour afficher la valeur de la propriété d’une tâche en cours d’exécution, vous devez vous connecter au service Planificateur de tâches, puis obtenir une collection de toutes les tâches en cours d’exécution (y compris ou excluant les tâches masquées).</span><span class="sxs-lookup"><span data-stu-id="c73bb-112">To display a running task's property value, you must connect to the Task Scheduler service, and then get a collection of all the running tasks (including or excluding hidden tasks).</span></span> <span data-ttu-id="c73bb-113">Ensuite, vous énumérez chaque tâche en cours d’exécution et récupérez et affichez une valeur de propriété pour chaque tâche.</span><span class="sxs-lookup"><span data-stu-id="c73bb-113">Then you enumerate through each running task and get and display a property value for each task.</span></span>

## <a name="example"></a><span data-ttu-id="c73bb-114">Exemple</span><span class="sxs-lookup"><span data-stu-id="c73bb-114">Example</span></span>

<span data-ttu-id="c73bb-115">Les exemples suivants énumèrent les tâches et affichent le nom et l’état des tâches :</span><span class="sxs-lookup"><span data-stu-id="c73bb-115">The following examples enumerate tasks and display the name and state of the tasks:</span></span>

-   [<span data-ttu-id="c73bb-116">Affichage des noms et des États des tâches (script)</span><span class="sxs-lookup"><span data-stu-id="c73bb-116">Displaying Task Names and States (Scripting)</span></span>](displaying-task-names-and-state--scripting-.md)
-   [<span data-ttu-id="c73bb-117">Affichage des noms et de l’état des tâches (C++)</span><span class="sxs-lookup"><span data-stu-id="c73bb-117">Displaying Task Names and State (C++)</span></span>](displaying-task-names-and-state--c---.md)

## <a name="related-topics"></a><span data-ttu-id="c73bb-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c73bb-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c73bb-119">Utilisation de l’Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="c73bb-119">Using the Task Scheduler</span></span>](using-the-task-scheduler.md)
</dt> </dl>

 

 




