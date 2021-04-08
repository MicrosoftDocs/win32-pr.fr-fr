---
description: L’application est divisée en deux programmes. L’un des programmes s’exécute en tant qu’utilisateur standard et l’autre s’exécute avec des privilèges d’administrateur.
ms.assetid: 1e661915-5797-421d-b96f-72949f441aba
title: Modèle de Broker administrateur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5299d35c995fb56f969fc5983864cfc93b25b6c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865998"
---
# <a name="administrator-broker-model"></a><span data-ttu-id="0c77f-104">Modèle de Broker administrateur</span><span class="sxs-lookup"><span data-stu-id="0c77f-104">Administrator Broker Model</span></span>

<span data-ttu-id="0c77f-105">Dans le modèle de Broker administrateur, l’application est divisée en deux programmes.</span><span class="sxs-lookup"><span data-stu-id="0c77f-105">In the administrator broker model, the application is divided into two programs.</span></span> <span data-ttu-id="0c77f-106">L’un des programmes s’exécute en tant qu’utilisateur standard et l’autre s’exécute avec des privilèges d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="0c77f-106">One of the programs runs as a standard user, and the other runs with administrator privilege.</span></span>

<span data-ttu-id="0c77f-107">À l’aide d’un manifeste d’application, marquez le programme utilisateur standard avec le **requestedExecutionLevel** de **asInvoker** et marquez le programme administratif avec un **requestedExecutionLevel** de **requireAdministrator**.</span><span class="sxs-lookup"><span data-stu-id="0c77f-107">Using an application manifest, mark the standard user program with a **requestedExecutionLevel** of **asInvoker** and mark the administrative program with a **requestedExecutionLevel** of **requireAdministrator**.</span></span> <span data-ttu-id="0c77f-108">Un utilisateur lance d’abord le programme utilisateur standard.</span><span class="sxs-lookup"><span data-stu-id="0c77f-108">A user launches the standard user program first.</span></span> <span data-ttu-id="0c77f-109">Lorsque l’utilisateur tente d’effectuer une opération qui requiert un jeton d’accès administrateur complet, le programme utilisateur standard appelle la fonction [**ShellExecute**](/windows/desktop/api/shellapi/nf-shellapi-shellexecutea) pour lancer le programme administratif.</span><span class="sxs-lookup"><span data-stu-id="0c77f-109">When the user attempts to perform an operation that requires a full administrator access token, the standard user program calls the [**ShellExecute**](/windows/desktop/api/shellapi/nf-shellapi-shellexecutea) function to launch the administrative program.</span></span> <span data-ttu-id="0c77f-110">La fonction **ShellExecute** invite l’utilisateur à approuver avant d’exécuter l’application avec le jeton d’accès administrateur complet de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="0c77f-110">The **ShellExecute** function prompts the user for approval before running the application with the user's full administrator access token.</span></span> <span data-ttu-id="0c77f-111">Le programme administratif peut ensuite effectuer des tâches qui requièrent des privilèges d’administrateur.</span><span class="sxs-lookup"><span data-stu-id="0c77f-111">The administrative program can then perform tasks that require administrator privilege.</span></span>

<span data-ttu-id="0c77f-112">Le programme d’administration n’est pas complètement isolé du programme utilisateur standard.</span><span class="sxs-lookup"><span data-stu-id="0c77f-112">The administrative program is not completely isolated from the standard user program.</span></span> <span data-ttu-id="0c77f-113">Le programme administratif peut activer la communication entre processus avec le programme utilisateur standard.</span><span class="sxs-lookup"><span data-stu-id="0c77f-113">The administrative program can enable interprocess communication with the standard user program.</span></span> <span data-ttu-id="0c77f-114">Toutefois, ces communications sont limitées par la stratégie d’intégrité obligatoire par défaut.</span><span class="sxs-lookup"><span data-stu-id="0c77f-114">However, such communication is limited by the default mandatory integrity policy.</span></span> <span data-ttu-id="0c77f-115">Pour plus d’informations sur les considérations relatives à l’intégrité obligatoire, consultez [conception d’applications pour qu’elles s’exécutent à un niveau d’intégrité faible](/previous-versions/dotnet/articles/bb625960(v=msdn.10)).</span><span class="sxs-lookup"><span data-stu-id="0c77f-115">For information about mandatory integrity considerations, see [Designing Applications to Run at a Low Integrity Level](/previous-versions/dotnet/articles/bb625960(v=msdn.10)).</span></span>

<span data-ttu-id="0c77f-116">Voici les utilisations possibles du modèle Broker administrateur :</span><span class="sxs-lookup"><span data-stu-id="0c77f-116">The following are possible uses for the administrator broker model:</span></span>

-   <span data-ttu-id="0c77f-117">Développement des assistants.</span><span class="sxs-lookup"><span data-stu-id="0c77f-117">Developing wizards.</span></span> <span data-ttu-id="0c77f-118">Quand un assistant matériel détermine qu’un pilote requis n’est pas installé sur l’ordinateur ou qu’il se trouve dans l’emplacement approuvé de l’entreprise, il appelle une application avec élévation de privilèges, avec la possibilité de déplacer un pilote dans le magasin de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="0c77f-118">When a hardware wizard determines that a required driver is not installed on the computer or located in the enterprise's approved location, it calls an elevated application with the ability to move a driver into the computer store.</span></span>
-   <span data-ttu-id="0c77f-119">Autorun.exe appelant Setup.exe.</span><span class="sxs-lookup"><span data-stu-id="0c77f-119">Autorun.exe calling Setup.exe.</span></span> <span data-ttu-id="0c77f-120">Lorsqu’un utilisateur exécute un logiciel à partir d’un CD, Autorun.exe, qui s’exécute en tant qu’utilisateur standard, démarre Setup.exe, qui s’exécute en tant qu’administrateur, pour installer le logiciel sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="0c77f-120">When a user runs software from a CD, Autorun.exe, which runs as a standard user, starts Setup.exe, which runs as an administrator, to install the software onto the computer.</span></span>

<span data-ttu-id="0c77f-121">Voici les inconvénients de l’utilisation du modèle Broker administrateur :</span><span class="sxs-lookup"><span data-stu-id="0c77f-121">The following are drawbacks to using the administrator broker model:</span></span>

-   <span data-ttu-id="0c77f-122">Les transitions entre l’application et l’application peuvent être confuses pour l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="0c77f-122">The transitions from application to application can be confusing to the user.</span></span> <span data-ttu-id="0c77f-123">Il peut être difficile d’informer l’utilisateur de la raison pour laquelle une nouvelle application s’affiche sur le moniteur.</span><span class="sxs-lookup"><span data-stu-id="0c77f-123">It can be difficult to inform the user why a new application appears on the monitor.</span></span>
-   <span data-ttu-id="0c77f-124">Il peut être difficile de transmettre des informations d’État entre les deux applications.</span><span class="sxs-lookup"><span data-stu-id="0c77f-124">It can be difficult to pass state information between the two applications.</span></span> <span data-ttu-id="0c77f-125">Par exemple, vous ne devez pas utiliser ce modèle pour transmettre des informations d’État entre un panneau de configuration utilisateur standard (CPL) et son homologue d’administrateur simplement pour autoriser le même CPL à avoir des fonctionnalités d’administration et d’utilisateur standard.</span><span class="sxs-lookup"><span data-stu-id="0c77f-125">For example, you would not use this model to pass state information between a standard user control panel (CPL) and its administrator counterpart simply to allow the same CPL to have administrative and standard user functionality.</span></span> <span data-ttu-id="0c77f-126">Le CPL standard de l’utilisateur devrait stocker son état quelque part.</span><span class="sxs-lookup"><span data-stu-id="0c77f-126">The standard user CPL would have to store its state somewhere.</span></span>
-   <span data-ttu-id="0c77f-127">Il peut y avoir un grand nombre de code répliqué lors du fractionnement des fonctionnalités entre deux programmes.</span><span class="sxs-lookup"><span data-stu-id="0c77f-127">There can be a lot of replicated code when splitting the functionality between two programs.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0c77f-128">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0c77f-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0c77f-129">Développement d’applications nécessitant des privilèges d’administrateur</span><span class="sxs-lookup"><span data-stu-id="0c77f-129">Developing Applications that Require Administrator Privilege</span></span>](developing-applications-that-require-administrator-privilege.md)
</dt> <dt>

[<span data-ttu-id="0c77f-130">Modèle d’objet COM administrateur</span><span class="sxs-lookup"><span data-stu-id="0c77f-130">Administrator COM Object Model</span></span>](administrator-com-object-model.md)
</dt> <dt>

[<span data-ttu-id="0c77f-131">Modèle de service du système d’exploitation</span><span class="sxs-lookup"><span data-stu-id="0c77f-131">Operating System Service Model</span></span>](operating-system-service-model.md)
</dt> <dt>

[<span data-ttu-id="0c77f-132">Modèle de tâche avec élévation de privilèges</span><span class="sxs-lookup"><span data-stu-id="0c77f-132">Elevated Task Model</span></span>](elevated-task-model.md)
</dt> </dl>

 

 
