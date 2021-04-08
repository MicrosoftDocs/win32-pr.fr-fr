---
title: Actions de tâche
description: Les éléments de travail exécutés par une tâche sont appelés actions. Une tâche peut avoir une seule action ou au maximum 32 actions. Sachez que lorsque plusieurs actions sont spécifiées, elles sont exécutées de manière séquentielle.
ms.assetid: 4cbe739d-4c4e-4469-8289-4be41b93950c
keywords:
- actions Planificateur de tâches
- actions Planificateur de tâches, Description
- actions Planificateur de tâches, exécuter l’action
- actions Planificateur de tâches, action du gestionnaire COM
- Planificateur de tâches d’exécution de l’action
- Action du gestionnaire COM Planificateur de tâches
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71003e2cea5febfab61617451f3b6ebef4a244a3
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/11/2020
ms.locfileid: "103680906"
---
# <a name="task-actions"></a><span data-ttu-id="fbff8-111">Actions de tâche</span><span class="sxs-lookup"><span data-stu-id="fbff8-111">Task Actions</span></span>

<span data-ttu-id="fbff8-112">Les éléments de travail exécutés par une tâche sont appelés actions.</span><span class="sxs-lookup"><span data-stu-id="fbff8-112">The work items performed by a task are called actions.</span></span> <span data-ttu-id="fbff8-113">Une tâche peut avoir une seule action ou au maximum 32 actions.</span><span class="sxs-lookup"><span data-stu-id="fbff8-113">A task can have a single action or a maximum of 32 actions.</span></span> <span data-ttu-id="fbff8-114">Sachez que lorsque plusieurs actions sont spécifiées, elles sont exécutées de manière séquentielle.</span><span class="sxs-lookup"><span data-stu-id="fbff8-114">Be aware that when multiple actions are specified, they are executed sequentially.</span></span>

## <a name="types-of-actions"></a><span data-ttu-id="fbff8-115">Types d'actions</span><span class="sxs-lookup"><span data-stu-id="fbff8-115">Types of Actions</span></span>

<span data-ttu-id="fbff8-116">Le tableau d’actions suivant décrit le type de travail ou les actions qui peuvent être accomplies par une tâche.</span><span class="sxs-lookup"><span data-stu-id="fbff8-116">The following table of actions describes the type of work or actions that can be accomplished by a task.</span></span>

| <span data-ttu-id="fbff8-117">Type d’action</span><span class="sxs-lookup"><span data-stu-id="fbff8-117">Type of Action</span></span>      | <span data-ttu-id="fbff8-118">Description</span><span class="sxs-lookup"><span data-stu-id="fbff8-118">Description</span></span>                                                             |
|---------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="fbff8-119">Action du comhandleur</span><span class="sxs-lookup"><span data-stu-id="fbff8-119">ComHandler Action</span></span>   | <span data-ttu-id="fbff8-120">Cette action déclenche un gestionnaire COM.</span><span class="sxs-lookup"><span data-stu-id="fbff8-120">This action fires a COM handler.</span></span>                                        |
| <span data-ttu-id="fbff8-121">Action d’exécution</span><span class="sxs-lookup"><span data-stu-id="fbff8-121">Exec Action</span></span>         | <span data-ttu-id="fbff8-122">Cette action exécute une opération de ligne de commande telle que le démarrage du bloc-notes.</span><span class="sxs-lookup"><span data-stu-id="fbff8-122">This action executes a command-line operation such as starting Notepad.</span></span> |
| <span data-ttu-id="fbff8-123">Action de messagerie</span><span class="sxs-lookup"><span data-stu-id="fbff8-123">E-mail Action</span></span>       | <span data-ttu-id="fbff8-124">Cette action envoie un message électronique lorsqu’une tâche est déclenchée.</span><span class="sxs-lookup"><span data-stu-id="fbff8-124">This action sends an email when a task is triggered.</span></span>                    |
| <span data-ttu-id="fbff8-125">Afficher l’action du message</span><span class="sxs-lookup"><span data-stu-id="fbff8-125">Show Message Action</span></span> | <span data-ttu-id="fbff8-126">Cette action affiche une boîte de message avec un message et un titre spécifiés.</span><span class="sxs-lookup"><span data-stu-id="fbff8-126">This action shows a message box with a specified message and title.</span></span>     |



 

## <a name="specifying-actions"></a><span data-ttu-id="fbff8-127">Spécification des actions</span><span class="sxs-lookup"><span data-stu-id="fbff8-127">Specifying Actions</span></span>

<span data-ttu-id="fbff8-128">Les actions d’une tâche sont spécifiées lorsque la tâche est définie et stockée dans une collection d’actions utilisées par le service Planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="fbff8-128">The actions of a task are specified when the task is defined and stored in a collection of actions used by the Task Scheduler service.</span></span> <span data-ttu-id="fbff8-129">Le tableau suivant répertorie des liens vers des rubriques de référence pour les API et les éléments XML associés à des actions.</span><span class="sxs-lookup"><span data-stu-id="fbff8-129">The following table lists links to reference topics for the APIs and XML elements that are associated with actions.</span></span>

<span data-ttu-id="fbff8-130">Pour plus d’informations et des exemples sur l’utilisation des interfaces Planificateur de tâches, les objets de script et XML, consultez [utilisation du planificateur de tâches](using-the-task-scheduler.md).</span><span class="sxs-lookup"><span data-stu-id="fbff8-130">For more information and examples about how to use the Task Scheduler interfaces, scripting objects, and XML, see [Using the Task Scheduler](using-the-task-scheduler.md).</span></span>

### <a name="interface-apis-for-c-development"></a><span data-ttu-id="fbff8-131">API d’interface pour le développement C++</span><span class="sxs-lookup"><span data-stu-id="fbff8-131">Interface APIs for C++ Development</span></span>



| <span data-ttu-id="fbff8-132">API</span><span class="sxs-lookup"><span data-stu-id="fbff8-132">API</span></span>                                                                    | <span data-ttu-id="fbff8-133">Description</span><span class="sxs-lookup"><span data-stu-id="fbff8-133">Description</span></span>                                                  |
|------------------------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="fbff8-134">**Propriété actions de ITaskDefinition**</span><span class="sxs-lookup"><span data-stu-id="fbff8-134">**Actions Property of ITaskDefinition**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_actions) | <span data-ttu-id="fbff8-135">Obtient ou définit les actions effectuées par la tâche.</span><span class="sxs-lookup"><span data-stu-id="fbff8-135">Gets or sets the actions performed by the task.</span></span>              |
| [<span data-ttu-id="fbff8-136">**IActionCollection**</span><span class="sxs-lookup"><span data-stu-id="fbff8-136">**IActionCollection**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-iactioncollection)                         | <span data-ttu-id="fbff8-137">Contient les actions effectuées par la tâche.</span><span class="sxs-lookup"><span data-stu-id="fbff8-137">Contains the actions performed by the task.</span></span>                  |
| [<span data-ttu-id="fbff8-138">**IComHandlerAction**</span><span class="sxs-lookup"><span data-stu-id="fbff8-138">**IComHandlerAction**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-icomhandleraction)                         | <span data-ttu-id="fbff8-139">Représente une action qui déclenche un gestionnaire.</span><span class="sxs-lookup"><span data-stu-id="fbff8-139">Represents an action that fires a handler.</span></span>                   |
| [<span data-ttu-id="fbff8-140">**IExecAction**</span><span class="sxs-lookup"><span data-stu-id="fbff8-140">**IExecAction**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-iexecaction)                                     | <span data-ttu-id="fbff8-141">Représente une action qui exécute une opération de ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="fbff8-141">Represents an action that executes a command-line operation.</span></span> |
| [<span data-ttu-id="fbff8-142">**IEmailAction**</span><span class="sxs-lookup"><span data-stu-id="fbff8-142">**IEmailAction**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-iemailaction)                                   | <span data-ttu-id="fbff8-143">Représente une action qui envoie un message électronique.</span><span class="sxs-lookup"><span data-stu-id="fbff8-143">Represents an action that sends an email message.</span></span>            |
| [<span data-ttu-id="fbff8-144">**IShowMessageAction**</span><span class="sxs-lookup"><span data-stu-id="fbff8-144">**IShowMessageAction**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-ishowmessageaction)                       | <span data-ttu-id="fbff8-145">Représente une action qui affiche une boîte de message.</span><span class="sxs-lookup"><span data-stu-id="fbff8-145">Represents an action that shows a message box.</span></span>               |



 

### <a name="scripting-object-apis-for-scripting-development"></a><span data-ttu-id="fbff8-146">Scripts des API objet pour le développement de scripts</span><span class="sxs-lookup"><span data-stu-id="fbff8-146">Scripting Object APIs for Scripting Development</span></span>



| <span data-ttu-id="fbff8-147">API</span><span class="sxs-lookup"><span data-stu-id="fbff8-147">API</span></span>                                                      | <span data-ttu-id="fbff8-148">Description</span><span class="sxs-lookup"><span data-stu-id="fbff8-148">Description</span></span>                                                  |
|----------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="fbff8-149">**TaskDefinition. actions**</span><span class="sxs-lookup"><span data-stu-id="fbff8-149">**TaskDefinition.Actions**</span></span>](taskdefinition-actions.md) | <span data-ttu-id="fbff8-150">Obtient ou définit les actions effectuées par la tâche.</span><span class="sxs-lookup"><span data-stu-id="fbff8-150">Gets or sets the actions performed by the task.</span></span>              |
| [<span data-ttu-id="fbff8-151">**ActionCollection**</span><span class="sxs-lookup"><span data-stu-id="fbff8-151">**ActionCollection**</span></span>](actioncollection.md)             | <span data-ttu-id="fbff8-152">Contient les actions effectuées par la tâche.</span><span class="sxs-lookup"><span data-stu-id="fbff8-152">Contains the actions performed by the task.</span></span>                  |
| [<span data-ttu-id="fbff8-153">**ComHandlerAction**</span><span class="sxs-lookup"><span data-stu-id="fbff8-153">**ComHandlerAction**</span></span>](comhandleraction.md)             | <span data-ttu-id="fbff8-154">Représente une action qui déclenche un gestionnaire.</span><span class="sxs-lookup"><span data-stu-id="fbff8-154">Represents an action that fires a handler.</span></span>                   |
| [<span data-ttu-id="fbff8-155">**ExecAction**</span><span class="sxs-lookup"><span data-stu-id="fbff8-155">**ExecAction**</span></span>](execaction.md)                         | <span data-ttu-id="fbff8-156">Représente une action qui exécute une opération de ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="fbff8-156">Represents an action that executes a command-line operation.</span></span> |
| [<span data-ttu-id="fbff8-157">**EmailAction**</span><span class="sxs-lookup"><span data-stu-id="fbff8-157">**EmailAction**</span></span>](emailaction.md)                       | <span data-ttu-id="fbff8-158">Représente une action qui envoie un message électronique.</span><span class="sxs-lookup"><span data-stu-id="fbff8-158">Represents an action that sends an email message.</span></span>            |
| [<span data-ttu-id="fbff8-159">**ShowMessageAction**</span><span class="sxs-lookup"><span data-stu-id="fbff8-159">**ShowMessageAction**</span></span>](showmessageaction.md)           | <span data-ttu-id="fbff8-160">Représente une action qui affiche une boîte de message.</span><span class="sxs-lookup"><span data-stu-id="fbff8-160">Represents an action that shows a message box.</span></span>               |



 

### <a name="xml-elements"></a><span data-ttu-id="fbff8-161">Éléments XML</span><span class="sxs-lookup"><span data-stu-id="fbff8-161">XML Elements</span></span>



| <span data-ttu-id="fbff8-162">Élément</span><span class="sxs-lookup"><span data-stu-id="fbff8-162">Element</span></span>                                                                    | <span data-ttu-id="fbff8-163">Description</span><span class="sxs-lookup"><span data-stu-id="fbff8-163">Description</span></span>                                                  |
|----------------------------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="fbff8-164">**Actions**</span><span class="sxs-lookup"><span data-stu-id="fbff8-164">**Actions**</span></span>](taskschedulerschema-actions-tasktype-element.md)            | <span data-ttu-id="fbff8-165">Définit les actions effectuées par la tâche.</span><span class="sxs-lookup"><span data-stu-id="fbff8-165">Defines the actions performed by the task.</span></span>                   |
| [<span data-ttu-id="fbff8-166">**Comgérer**</span><span class="sxs-lookup"><span data-stu-id="fbff8-166">**ComHandler**</span></span>](taskschedulerschema-comhandler-actiongroup-element.md)   | <span data-ttu-id="fbff8-167">Représente une action qui déclenche un gestionnaire.</span><span class="sxs-lookup"><span data-stu-id="fbff8-167">Represents an action that fires a handler.</span></span>                   |
| [<span data-ttu-id="fbff8-168">**Exécutable**</span><span class="sxs-lookup"><span data-stu-id="fbff8-168">**Exec**</span></span>](taskschedulerschema-exec-actiongroup-element.md)               | <span data-ttu-id="fbff8-169">Représente une action qui exécute une opération de ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="fbff8-169">Represents an action that executes a command-line operation.</span></span> |
| [<span data-ttu-id="fbff8-170">**SendEmail**</span><span class="sxs-lookup"><span data-stu-id="fbff8-170">**SendEmail**</span></span>](taskschedulerschema-sendemail-actiongroup-element.md)     | <span data-ttu-id="fbff8-171">Représente une action qui envoie un message électronique.</span><span class="sxs-lookup"><span data-stu-id="fbff8-171">Represents an action that sends an email message.</span></span>            |
| [<span data-ttu-id="fbff8-172">**ShowMessage**</span><span class="sxs-lookup"><span data-stu-id="fbff8-172">**ShowMessage**</span></span>](taskschedulerschema-showmessage-actiongroup-element.md) | <span data-ttu-id="fbff8-173">Représente une action qui affiche une boîte de message.</span><span class="sxs-lookup"><span data-stu-id="fbff8-173">Represents an action that shows a message box.</span></span>               |



 

## <a name="using-variables-in-action-properties"></a><span data-ttu-id="fbff8-174">Utilisation de variables dans les propriétés d’action</span><span class="sxs-lookup"><span data-stu-id="fbff8-174">Using Variables in Action Properties</span></span>

<span data-ttu-id="fbff8-175">Certaines propriétés d’action qui sont de type **BSTR** peuvent contenir des variables $ (arg0), $ (Arg1),..., $ (Arg32) dans leurs valeurs de chaîne.</span><span class="sxs-lookup"><span data-stu-id="fbff8-175">Some action properties that are of type **BSTR** can contain $(Arg0), $(Arg1), ..., $(Arg32) variables in their string values.</span></span> <span data-ttu-id="fbff8-176">Ces variables sont remplacées par les valeurs spécifiées dans le paramètre *params* des méthodes [**IRegisteredTask :: Run**](/windows/desktop/api/taskschd/nf-taskschd-iregisteredtask-run) et [**IRegisteredTask :: RunEx**](/windows/desktop/api/taskschd/nf-taskschd-iregisteredtask-runex) ou sont contenues dans le déclencheur d’événement pour la tâche.</span><span class="sxs-lookup"><span data-stu-id="fbff8-176">These variables are replaced with the values that are specified in the *params* parameter of the [**IRegisteredTask::Run**](/windows/desktop/api/taskschd/nf-taskschd-iregisteredtask-run) and [**IRegisteredTask::RunEx**](/windows/desktop/api/taskschd/nf-taskschd-iregisteredtask-runex) methods or are contained within the event trigger for the task.</span></span> <span data-ttu-id="fbff8-177">Le tableau suivant répertorie les propriétés d’action qui peuvent utiliser des variables dans leurs valeurs de chaîne.</span><span class="sxs-lookup"><span data-stu-id="fbff8-177">The following table lists the action properties that can use variables in their string values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="fbff8-178">Action</span><span class="sxs-lookup"><span data-stu-id="fbff8-178">Action</span></span></th>
<th><span data-ttu-id="fbff8-179">Propriétés</span><span class="sxs-lookup"><span data-stu-id="fbff8-179">Properties</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="fbff8-180">Action du gestionnaire COM</span><span class="sxs-lookup"><span data-stu-id="fbff8-180">COM Handler Action</span></span></td>
<td><span data-ttu-id="fbff8-181">C++ :</span><span class="sxs-lookup"><span data-stu-id="fbff8-181">C++:</span></span>
<ul>
<li><span data-ttu-id="fbff8-182"><a href="/windows/desktop/api/taskschd/nf-taskschd-icomhandleraction-get_classid"><strong>Propriété ClassId de IComHandlerAction</strong></a></span><span class="sxs-lookup"><span data-stu-id="fbff8-182"><a href="/windows/desktop/api/taskschd/nf-taskschd-icomhandleraction-get_classid"><strong>ClassId Property of IComHandlerAction</strong></a></span></span></li>
<li><span data-ttu-id="fbff8-183"><a href="/windows/desktop/api/taskschd/nf-taskschd-icomhandleraction-get_data"><strong>Propriété de données de IComHandlerAction</strong></a></span><span class="sxs-lookup"><span data-stu-id="fbff8-183"><a href="/windows/desktop/api/taskschd/nf-taskschd-icomhandleraction-get_data"><strong>Data Property of IComHandlerAction</strong></a></span></span></li>
</ul>
<br/> <span data-ttu-id="fbff8-184">Création de scripts :</span><span class="sxs-lookup"><span data-stu-id="fbff8-184">Scripting:</span></span>
<ul>
<li><span data-ttu-id="fbff8-185"><a href="comhandleraction-classid.md"><strong>ComHandlerAction. ClassId</strong></a></span><span class="sxs-lookup"><span data-stu-id="fbff8-185"><a href="comhandleraction-classid.md"><strong>ComHandlerAction.ClassId</strong></a></span></span></li>
<li><span data-ttu-id="fbff8-186"><a href="comhandleraction-data.md"><strong>ComHandlerAction. Data</strong></a></span><span class="sxs-lookup"><span data-stu-id="fbff8-186"><a href="comhandleraction-data.md"><strong>ComHandlerAction.Data</strong></a></span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fbff8-187">Action de messagerie</span><span class="sxs-lookup"><span data-stu-id="fbff8-187">Email Action</span></span></td>
<td><span data-ttu-id="fbff8-188">C++ :</span><span class="sxs-lookup"><span data-stu-id="fbff8-188">C++:</span></span>
<ul>
<li><span data-ttu-id="fbff8-189"><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_body"><strong>Propriété Body de IEmailAction</strong></a></span><span class="sxs-lookup"><span data-stu-id="fbff8-189"><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_body"><strong>Body Property of IEmailAction</strong></a></span></span></li>
<li><span data-ttu-id="fbff8-190"><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_server"><strong>Propriété Server de IEmailAction</strong></a></span><span class="sxs-lookup"><span data-stu-id="fbff8-190"><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_server"><strong>Server Property of IEmailAction</strong></a></span></span></li>
<li><span data-ttu-id="fbff8-191"><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_subject"><strong>Propriété Subject de IEmailAction</strong></a></span><span class="sxs-lookup"><span data-stu-id="fbff8-191"><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_subject"><strong>Subject Property of IEmailAction</strong></a></span></span></li>
<li><span data-ttu-id="fbff8-192"><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_to"><strong>À la propriété de IEmailAction</strong></a></span><span class="sxs-lookup"><span data-stu-id="fbff8-192"><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_to"><strong>To Property of IEmailAction</strong></a></span></span></li>
<li><span data-ttu-id="fbff8-193"><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_cc"><strong>Propriété CC de IEmailAction</strong></a></span><span class="sxs-lookup"><span data-stu-id="fbff8-193"><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_cc"><strong>Cc Property of IEmailAction</strong></a></span></span></li>
<li><span data-ttu-id="fbff8-194"><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_bcc"><strong>Propriété BCC de IEmailAction</strong></a></span><span class="sxs-lookup"><span data-stu-id="fbff8-194"><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_bcc"><strong>Bcc Property of IEmailAction</strong></a></span></span></li>
<li><span data-ttu-id="fbff8-195"><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_replyto"><strong>Propriété ReplyTo de IEmailAction</strong></a></span><span class="sxs-lookup"><span data-stu-id="fbff8-195"><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_replyto"><strong>ReplyTo Property of IEmailAction</strong></a></span></span></li>
<li><span data-ttu-id="fbff8-196"><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_from"><strong>De la propriété de IEmailAction</strong></a></span><span class="sxs-lookup"><span data-stu-id="fbff8-196"><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_from"><strong>From Property of IEmailAction</strong></a></span></span></li>
</ul>
<br/> <span data-ttu-id="fbff8-197">Création de scripts :</span><span class="sxs-lookup"><span data-stu-id="fbff8-197">Scripting:</span></span>
<ul>
<li><span data-ttu-id="fbff8-198"><a href="emailaction-body.md"><strong>EmailAction. Body</strong></a></span><span class="sxs-lookup"><span data-stu-id="fbff8-198"><a href="emailaction-body.md"><strong>EmailAction.Body</strong></a></span></span></li>
<li><span data-ttu-id="fbff8-199"><a href="emailaction-server.md"><strong>EmailAction. Server</strong></a></span><span class="sxs-lookup"><span data-stu-id="fbff8-199"><a href="emailaction-server.md"><strong>EmailAction.Server</strong></a></span></span></li>
<li><span data-ttu-id="fbff8-200"><a href="emailaction-subject.md"><strong>EmailAction. Subject</strong></a></span><span class="sxs-lookup"><span data-stu-id="fbff8-200"><a href="emailaction-subject.md"><strong>EmailAction.Subject</strong></a></span></span></li>
<li><span data-ttu-id="fbff8-201"><a href="emailaction-to.md"><strong>EmailAction.To</strong></a></span><span class="sxs-lookup"><span data-stu-id="fbff8-201"><a href="emailaction-to.md"><strong>EmailAction.To</strong></a></span></span></li>
<li><span data-ttu-id="fbff8-202"><a href="emailaction-cc.md"><strong>EmailAction.Cc</strong></a></span><span class="sxs-lookup"><span data-stu-id="fbff8-202"><a href="emailaction-cc.md"><strong>EmailAction.Cc</strong></a></span></span></li>
<li><span data-ttu-id="fbff8-203"><a href="emailaction-bcc.md"><strong>EmailAction. CCI</strong></a></span><span class="sxs-lookup"><span data-stu-id="fbff8-203"><a href="emailaction-bcc.md"><strong>EmailAction.Bcc</strong></a></span></span></li>
<li><span data-ttu-id="fbff8-204"><a href="emailaction-replyto.md"><strong>EmailAction. ReplyTo</strong></a></span><span class="sxs-lookup"><span data-stu-id="fbff8-204"><a href="emailaction-replyto.md"><strong>EmailAction.ReplyTo</strong></a></span></span></li>
<li><span data-ttu-id="fbff8-205"><a href="emailaction-from.md"><strong>EmailAction. from</strong></a></span><span class="sxs-lookup"><span data-stu-id="fbff8-205"><a href="emailaction-from.md"><strong>EmailAction.From</strong></a></span></span></li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="fbff8-206">Action d’exécution</span><span class="sxs-lookup"><span data-stu-id="fbff8-206">Exec Action</span></span></td>
<td><span data-ttu-id="fbff8-207">C++ :</span><span class="sxs-lookup"><span data-stu-id="fbff8-207">C++:</span></span>
<ul>
<li><span data-ttu-id="fbff8-208"><a href="/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_arguments"><strong>Propriété arguments de IExecAction</strong></a></span><span class="sxs-lookup"><span data-stu-id="fbff8-208"><a href="/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_arguments"><strong>Arguments Property of IExecAction</strong></a></span></span></li>
<li><span data-ttu-id="fbff8-209"><a href="/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_workingdirectory"><strong>Propriété WorkingDirectory de IExecAction</strong></a></span><span class="sxs-lookup"><span data-stu-id="fbff8-209"><a href="/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_workingdirectory"><strong>WorkingDirectory Property of IExecAction</strong></a></span></span></li>
</ul>
<br/> <span data-ttu-id="fbff8-210">Création de scripts :</span><span class="sxs-lookup"><span data-stu-id="fbff8-210">Scripting:</span></span>
<ul>
<li><span data-ttu-id="fbff8-211"><a href="execaction-arguments.md"><strong>ExecAction. arguments</strong></a></span><span class="sxs-lookup"><span data-stu-id="fbff8-211"><a href="execaction-arguments.md"><strong>ExecAction.Arguments</strong></a></span></span></li>
<li><span data-ttu-id="fbff8-212"><a href="execaction-workingdirectory.md"><strong>ExecAction. WorkingDirectory</strong></a></span><span class="sxs-lookup"><span data-stu-id="fbff8-212"><a href="execaction-workingdirectory.md"><strong>ExecAction.WorkingDirectory</strong></a></span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="fbff8-213">Afficher l’action du message</span><span class="sxs-lookup"><span data-stu-id="fbff8-213">Show Message Action</span></span></td>
<td><span data-ttu-id="fbff8-214">C++ :</span><span class="sxs-lookup"><span data-stu-id="fbff8-214">C++:</span></span>
<ul>
<li><span data-ttu-id="fbff8-215"><a href="/windows/desktop/api/taskschd/nf-taskschd-ishowmessageaction-get_title"><strong>Propriété Title de IShowMessageAction</strong></a></span><span class="sxs-lookup"><span data-stu-id="fbff8-215"><a href="/windows/desktop/api/taskschd/nf-taskschd-ishowmessageaction-get_title"><strong>Title Property of IShowMessageAction</strong></a></span></span></li>
<li><span data-ttu-id="fbff8-216"><a href="/windows/desktop/api/taskschd/nf-taskschd-ishowmessageaction-get_messagebody"><strong>Propriété MessageBody de IShowMessageAction</strong></a></span><span class="sxs-lookup"><span data-stu-id="fbff8-216"><a href="/windows/desktop/api/taskschd/nf-taskschd-ishowmessageaction-get_messagebody"><strong>MessageBody Property of IShowMessageAction</strong></a></span></span></li>
</ul>
<br/> <span data-ttu-id="fbff8-217">Création de scripts :</span><span class="sxs-lookup"><span data-stu-id="fbff8-217">Scripting:</span></span>
<ul>
<li><span data-ttu-id="fbff8-218"><a href="showmessageaction-title.md"><strong>ShowMessageAction. title</strong></a></span><span class="sxs-lookup"><span data-stu-id="fbff8-218"><a href="showmessageaction-title.md"><strong>ShowMessageAction.Title</strong></a></span></span></li>
<li><span data-ttu-id="fbff8-219"><a href="showmessageaction-messagebody.md"><strong>ShowMessageAction. MessageBody</strong></a></span><span class="sxs-lookup"><span data-stu-id="fbff8-219"><a href="showmessageaction-messagebody.md"><strong>ShowMessageAction.MessageBody</strong></a></span></span></li>
</ul>
<br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="fbff8-220">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fbff8-220">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fbff8-221">À propos de l’Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="fbff8-221">About The Task Scheduler</span></span>](about-the-task-scheduler.md)
</dt> </dl>

 

 





