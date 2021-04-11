---
description: Une application s’exécutant en tant qu’utilisateur standard effectue des opérations qui requièrent des privilèges d’administrateur en démarrant une tâche planifiée.
ms.assetid: cd7485b3-6be5-4163-9a86-7892dbc59181
title: Modèle de tâche avec élévation de privilèges
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27006e32210cfea05de5c2b3b9adf36613dc4f5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320549"
---
# <a name="elevated-task-model"></a><span data-ttu-id="9d1b9-103">Modèle de tâche avec élévation de privilèges</span><span class="sxs-lookup"><span data-stu-id="9d1b9-103">Elevated Task Model</span></span>

<span data-ttu-id="9d1b9-104">Dans le modèle de tâche avec élévation de privilèges, une application qui s’exécute en tant qu’utilisateur standard effectue des opérations qui requièrent des privilèges d’administrateur en démarrant une tâche planifiée.</span><span class="sxs-lookup"><span data-stu-id="9d1b9-104">In the elevated task model, an application running as a standard user performs operations that require administrator privilege by starting a scheduled task.</span></span>

<span data-ttu-id="9d1b9-105">**Windows Server 2003 et Windows XP :** Le modèle de tâche avec élévation de privilèges n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="9d1b9-105">**Windows Server 2003 and Windows XP:** The elevated task model is not supported.</span></span>

<span data-ttu-id="9d1b9-106">Les tâches ne consomment pas autant de ressources système que de services et les tâches se ferment automatiquement lorsqu’elles sont terminées.</span><span class="sxs-lookup"><span data-stu-id="9d1b9-106">Tasks do not consume as many system resources as services, and tasks automatically close when finished.</span></span> <span data-ttu-id="9d1b9-107">Envisagez d’utiliser ce modèle au lieu du [modèle de service du système d’exploitation](operating-system-service-model.md) , sauf si la compatibilité descendante avec les systèmes d’exploitation antérieurs est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="9d1b9-107">Consider using this model instead of the [Operating System Service Model](operating-system-service-model.md) unless backward compatibility with earlier operating systems is necessary.</span></span>

<span data-ttu-id="9d1b9-108">Pour utiliser une tâche afin d’effectuer des opérations privilégiées pour une application utilisateur standard, les conditions suivantes doivent être remplies :</span><span class="sxs-lookup"><span data-stu-id="9d1b9-108">To use a task to perform privileged operations for a standard user application, the following conditions must be met:</span></span>

-   <span data-ttu-id="9d1b9-109">La tâche doit être définie pour s’exécuter en tant que **système**.</span><span class="sxs-lookup"><span data-stu-id="9d1b9-109">The task must be set to run as **SYSTEM**.</span></span>
-   <span data-ttu-id="9d1b9-110">Le [*descripteur de sécurité*](/windows/desktop/SecGloss/s-gly) associé à la tâche doit être configuré pour permettre aux utilisateurs standard de démarrer la tâche.</span><span class="sxs-lookup"><span data-stu-id="9d1b9-110">The [*security descriptor*](/windows/desktop/SecGloss/s-gly) associated with the task must be configured to allow standard users to start the task.</span></span>
-   <span data-ttu-id="9d1b9-111">Le service du planificateur de tâches doit être en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="9d1b9-111">The task scheduler service must be running.</span></span>

<span data-ttu-id="9d1b9-112">Pour plus d’informations sur la création et le démarrage de tâches, consultez [Planificateur de tâches](/windows/desktop/TaskSchd/task-scheduler-start-page).</span><span class="sxs-lookup"><span data-stu-id="9d1b9-112">For information about how to create and start tasks, see [Task Scheduler](/windows/desktop/TaskSchd/task-scheduler-start-page).</span></span>

## <a name="related-topics"></a><span data-ttu-id="9d1b9-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9d1b9-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9d1b9-114">Développement d’applications nécessitant des privilèges d’administrateur</span><span class="sxs-lookup"><span data-stu-id="9d1b9-114">Developing Applications that Require Administrator Privilege</span></span>](developing-applications-that-require-administrator-privilege.md)
</dt> <dt>

[<span data-ttu-id="9d1b9-115">Modèle de Broker administrateur</span><span class="sxs-lookup"><span data-stu-id="9d1b9-115">Administrator Broker Model</span></span>](administrator-broker-model.md)
</dt> <dt>

[<span data-ttu-id="9d1b9-116">Modèle d’objet COM administrateur</span><span class="sxs-lookup"><span data-stu-id="9d1b9-116">Administrator COM Object Model</span></span>](administrator-com-object-model.md)
</dt> <dt>

[<span data-ttu-id="9d1b9-117">Modèle de service du système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="9d1b9-117">Operating System Service Model</span></span>](operating-system-service-model.md)
</dt> </dl>

 

 
