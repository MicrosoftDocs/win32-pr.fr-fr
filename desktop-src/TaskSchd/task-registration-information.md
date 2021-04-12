---
title: Informations d’inscription de la tâche
description: Les informations d’inscription permettent d’identifier une tâche de différentes façons. Par exemple, une tâche peut être identifiée par l’auteur, comment elle a été créée (appelée « source de tâche ») et la date d’inscription.
ms.assetid: 45c9fa99-2718-4202-8987-4b506bd677e9
keywords:
- informations d’inscription Planificateur de tâches
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed6c5048e9cbb9b41abcd9052a02371cd575b57c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309194"
---
# <a name="task-registration-information"></a><span data-ttu-id="0eddc-105">Informations d’inscription de la tâche</span><span class="sxs-lookup"><span data-stu-id="0eddc-105">Task Registration Information</span></span>

<span data-ttu-id="0eddc-106">Les informations d’inscription permettent d’identifier une tâche de différentes façons.</span><span class="sxs-lookup"><span data-stu-id="0eddc-106">Registration information provides a way to identify a task in several different ways.</span></span> <span data-ttu-id="0eddc-107">Par exemple, une tâche peut être identifiée par l’auteur, comment elle a été créée (appelée « source de tâche ») et la date d’inscription.</span><span class="sxs-lookup"><span data-stu-id="0eddc-107">For example, a task can be identified by the author, how it was authored (referred to as the task source), and date of registration.</span></span>

## <a name="using-registration-information"></a><span data-ttu-id="0eddc-108">Utilisation des informations d’inscription</span><span class="sxs-lookup"><span data-stu-id="0eddc-108">Using Registration Information</span></span>

<span data-ttu-id="0eddc-109">Les informations d’inscription sont généralement spécifiées lors de la création de la tâche, puis utilisées de la façon suivante :</span><span class="sxs-lookup"><span data-stu-id="0eddc-109">Registration information is typically specified when the task is created and then used in the following ways:</span></span>

-   <span data-ttu-id="0eddc-110">Affiché par l’interface utilisateur Planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="0eddc-110">Displayed by the Task Scheduler user interface.</span></span>
-   <span data-ttu-id="0eddc-111">Obtient ou définit par les applications ou les scripts C++.</span><span class="sxs-lookup"><span data-stu-id="0eddc-111">Get or set by C++ applications or scripts.</span></span>
-   <span data-ttu-id="0eddc-112">Dans un environnement d’entreprise, utilisé comme critère de recherche lors de l’énumération de toutes les tâches inscrites.</span><span class="sxs-lookup"><span data-stu-id="0eddc-112">In an enterprise environment, used as a search criteria when enumerating over all registered tasks.</span></span>

## <a name="types-of-registration-information"></a><span data-ttu-id="0eddc-113">Types d’informations d’inscription</span><span class="sxs-lookup"><span data-stu-id="0eddc-113">Types of Registration Information</span></span>

<span data-ttu-id="0eddc-114">Les informations d’inscription des tâches sont définies par les propriétés de l’objet [**RegistrationInfo**](registrationinfo.md) pour les applications de script, les propriétés de l’interface [**IRegistrationInfo**](/windows/desktop/api/taskschd/nn-taskschd-iregistrationinfo) pour les applications C++ et les éléments enfants de l' [**élément RegistrationInfo (TaskType)**](taskschedulerschema-registrationinfo-tasktype-element.md) pour la lecture ou l’écriture de code XML.</span><span class="sxs-lookup"><span data-stu-id="0eddc-114">Task registration information is defined by the properties of the [**RegistrationInfo**](registrationinfo.md) object for scripting applications, the properties of the [**IRegistrationInfo**](/windows/desktop/api/taskschd/nn-taskschd-iregistrationinfo) interface for C++ applications, and the child elements of the [**RegistrationInfo (taskType) element**](taskschedulerschema-registrationinfo-tasktype-element.md) for reading or writing XML.</span></span>

<span data-ttu-id="0eddc-115">Ces propriétés autorisent l’accès aux types d’informations d’inscription suivants :</span><span class="sxs-lookup"><span data-stu-id="0eddc-115">These properties allow access to the following types of registration information:</span></span>

-   <span data-ttu-id="0eddc-116">Auteur de la tâche</span><span class="sxs-lookup"><span data-stu-id="0eddc-116">Task Author</span></span>

    <span data-ttu-id="0eddc-117">Planificateur de tâches définit l’auteur de la tâche lors de sa création.</span><span class="sxs-lookup"><span data-stu-id="0eddc-117">Task Scheduler sets the author of the task when it is created.</span></span>

-   <span data-ttu-id="0eddc-118">Date d’inscription de la tâche</span><span class="sxs-lookup"><span data-stu-id="0eddc-118">Task Registration Date</span></span>

    <span data-ttu-id="0eddc-119">Planificateur de tâches définit cette date lorsque la tâche est inscrite.</span><span class="sxs-lookup"><span data-stu-id="0eddc-119">Task Scheduler sets this date when the task is registered.</span></span>

-   <span data-ttu-id="0eddc-120">Description de la tâche</span><span class="sxs-lookup"><span data-stu-id="0eddc-120">Task Description</span></span>

    <span data-ttu-id="0eddc-121">Description définie par l’utilisateur qui peut inclure les déclencheurs utilisés pour démarrer la tâche ou les actions effectuées par la tâche.</span><span class="sxs-lookup"><span data-stu-id="0eddc-121">A user-defined description that may include what triggers are used to start the task or what actions the task performs.</span></span>

-   <span data-ttu-id="0eddc-122">Documentation sur les tâches</span><span class="sxs-lookup"><span data-stu-id="0eddc-122">Task Documentation</span></span>

    <span data-ttu-id="0eddc-123">Documentation fournie par l’utilisateur et exigée par la tâche.</span><span class="sxs-lookup"><span data-stu-id="0eddc-123">User-supplied documentation that is needed by the task.</span></span>

-   <span data-ttu-id="0eddc-124">Descripteur de sécurité des tâches</span><span class="sxs-lookup"><span data-stu-id="0eddc-124">Task Security Descriptor</span></span>

    <span data-ttu-id="0eddc-125">Descripteur de sécurité fourni par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="0eddc-125">A user-supplied security descriptor.</span></span>

-   <span data-ttu-id="0eddc-126">Source de la tâche</span><span class="sxs-lookup"><span data-stu-id="0eddc-126">Task Source</span></span>

    <span data-ttu-id="0eddc-127">Informations fournies par l’utilisateur qui décrivent l’origine de la tâche.</span><span class="sxs-lookup"><span data-stu-id="0eddc-127">User-supplied information that describes where the task originated from.</span></span> <span data-ttu-id="0eddc-128">Par exemple, une tâche peut provenir d’un composant, d’un service, d’une application ou d’un utilisateur.</span><span class="sxs-lookup"><span data-stu-id="0eddc-128">For example, a task may originate from a component, service, application, or user.</span></span>

-   <span data-ttu-id="0eddc-129">URI de tâche</span><span class="sxs-lookup"><span data-stu-id="0eddc-129">Task URI</span></span>

    <span data-ttu-id="0eddc-130">URI (Uniform Resource Identifier) de la tâche.</span><span class="sxs-lookup"><span data-stu-id="0eddc-130">A uniform resource identifier (URI) for the task.</span></span>

-   <span data-ttu-id="0eddc-131">Version de la tâche</span><span class="sxs-lookup"><span data-stu-id="0eddc-131">Task Version</span></span>

    <span data-ttu-id="0eddc-132">Informations fournies par l’utilisateur qui sont utilisées lorsque plusieurs versions d’une tâche existent.</span><span class="sxs-lookup"><span data-stu-id="0eddc-132">User-supplied information that is used when multiple versions of a task exist.</span></span>

-   <span data-ttu-id="0eddc-133">Texte XML</span><span class="sxs-lookup"><span data-stu-id="0eddc-133">XML Text</span></span>

    <span data-ttu-id="0eddc-134">Version au format XML des informations d’inscription.</span><span class="sxs-lookup"><span data-stu-id="0eddc-134">An XML-formatted version of the registration information.</span></span> <span data-ttu-id="0eddc-135">Notez que vous pouvez définir ou modifier les informations d’inscription directement par le biais de ce code XML, et que les propriétés de l’objet et de l’interface appropriées seront mises à jour en conséquence.</span><span class="sxs-lookup"><span data-stu-id="0eddc-135">Note that you can set or modify the registration information directly through this XML and the appropriate object and interface properties will be updated accordingly.</span></span>

## <a name="registering-tasks"></a><span data-ttu-id="0eddc-136">Inscription de tâches</span><span class="sxs-lookup"><span data-stu-id="0eddc-136">Registering Tasks</span></span>

<span data-ttu-id="0eddc-137">Une tâche peut être inscrite après la création des définitions de tâche, et les informations d’inscription et les valeurs de paramètres sont fournies par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="0eddc-137">A task can be registered after the task definitions are created and registration information and setting values are supplied by the user.</span></span> <span data-ttu-id="0eddc-138">Une tâche est inscrite à l’aide de la méthode [**TaskFolder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) pour les applications de script ou de la méthode [**ITaskFolder :: RegisterTaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition) pour les applications C++.</span><span class="sxs-lookup"><span data-stu-id="0eddc-138">A task is registered using the [**TaskFolder.RegisterTaskDefinition**](taskfolder-registertaskdefinition.md) method for scripting applications or the [**ITaskFolder::RegisterTaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition) method for C++ applications.</span></span> <span data-ttu-id="0eddc-139">Si vous souhaitez inscrire une tâche à l’aide de XML pour définir la tâche, utilisez la méthode [**TaskFolder. RegisterTask**](taskfolder-registertask.md) pour les applications de script et la méthode [**ITaskFolder :: RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) pour les applications C++.</span><span class="sxs-lookup"><span data-stu-id="0eddc-139">If you want to register a task using XML to define the task, you use the [**TaskFolder.RegisterTask**](taskfolder-registertask.md) method for scripting applications and the [**ITaskFolder::RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) method for C++ applications.</span></span>

<span data-ttu-id="0eddc-140">Dans les méthodes mentionnées ci-dessus, vous pouvez spécifier le contexte de sécurité pour l’exécution de la tâche.</span><span class="sxs-lookup"><span data-stu-id="0eddc-140">In the methods mentioned above, you can specify the security context to run the task.</span></span> <span data-ttu-id="0eddc-141">Vous devez être administrateur sur le système pour planifier l’exécution des tâches sous des contextes autres que les vôtres.</span><span class="sxs-lookup"><span data-stu-id="0eddc-141">You have to be an administrator on the system to schedule jobs to run under contexts other than your own.</span></span> <span data-ttu-id="0eddc-142">Pour plus d’informations sur les contextes de sécurité pour exécuter des tâches, consultez [contextes de sécurité pour les tâches en cours d’exécution](security-contexts-for-running-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="0eddc-142">For more information on the security contexts to run tasks, see [Security Contexts for Running Tasks](security-contexts-for-running-tasks.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="0eddc-143">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0eddc-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0eddc-144">À propos de l’Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="0eddc-144">About The Task Scheduler</span></span>](about-the-task-scheduler.md)
</dt> <dt>

[<span data-ttu-id="0eddc-145">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="0eddc-145">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 




