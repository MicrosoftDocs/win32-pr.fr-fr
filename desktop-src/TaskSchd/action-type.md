---
title: Action. type, propriété
description: Pour les scripts, obtient le type de l’action.
ms.assetid: 6a0bca3d-9016-4167-9f6e-2cc95bafdb95
keywords:
- Planificateur de tâches de propriété de type
- Planificateur de tâches de propriété de type, objet d’action
- Planificateur de tâches de l’objet action, propriété type
topic_type:
- apiref
api_name:
- Action.Type
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3db8ca46a80503136c5fbbe1240cba6c664bc1a1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466038"
---
# <a name="actiontype-property"></a><span data-ttu-id="3f932-106">Action. type, propriété</span><span class="sxs-lookup"><span data-stu-id="3f932-106">Action.Type property</span></span>

<span data-ttu-id="3f932-107">Pour les scripts, obtient le type de l’action.</span><span class="sxs-lookup"><span data-stu-id="3f932-107">For scripting, gets the type of the action.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f932-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3f932-108">Syntax</span></span>


```VB
Action.Type As Integer
```



## <a name="property-value"></a><span data-ttu-id="3f932-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="3f932-109">Property value</span></span>

<span data-ttu-id="3f932-110">Cette propriété retourne l’une des constantes d’énumération de [**\_ \_ type d’action de tâche**](/windows/desktop/api/taskschd/ne-taskschd-task_action_type) suivantes.</span><span class="sxs-lookup"><span data-stu-id="3f932-110">This property returns one of the following [**TASK\_ACTION\_TYPE**](/windows/desktop/api/taskschd/ne-taskschd-task_action_type) enumeration constants.</span></span>



| <span data-ttu-id="3f932-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="3f932-111">Value</span></span>                                                                                                                                                                                                                                                   | <span data-ttu-id="3f932-112">Signification</span><span class="sxs-lookup"><span data-stu-id="3f932-112">Meaning</span></span>                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_ACTION_EXEC"></span><span id="task_action_exec"></span><dl> <span data-ttu-id="3f932-113"><dt>**Tâche \_ ACTION \_ Exec**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="3f932-113"><dt>**TASK\_ACTION\_EXEC**</dt> <dt>0</dt></span></span> </dl>                          | <span data-ttu-id="3f932-114">Cette action effectue une opération de ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="3f932-114">This action performs a command-line operation.</span></span> <span data-ttu-id="3f932-115">Par exemple, l’action peut exécuter un script, lancer un exécutable ou, si le nom d’un document est fourni, Rechercher l’application associée et lancer l’application avec le document.</span><span class="sxs-lookup"><span data-stu-id="3f932-115">For example, the action could run a script, launch an executable, or, if the name of a document is provided, find its associated application and launch the application with the document.</span></span><br/> |
| <span id="TASK_ACTION_COM_HANDLER"></span><span id="task_action_com_handler"></span><dl> <span data-ttu-id="3f932-116"><dt>**Tâche \_ \_ \_ Gestionnaire com d’action**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="3f932-116"><dt>**TASK\_ACTION\_COM\_HANDLER**</dt> <dt>5</dt></span></span> </dl>    | <span data-ttu-id="3f932-117">Cette action déclenche un gestionnaire.</span><span class="sxs-lookup"><span data-stu-id="3f932-117">This action fires a handler.</span></span><br/>                                                                                                                                                                                                              |
| <span id="TASK_ACTION_SEND_EMAIL"></span><span id="task_action_send_email"></span><dl> <span data-ttu-id="3f932-118"><dt>**Tâche \_ ACTION \_ Envoyer un \_ e-mail**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="3f932-118"><dt>**TASK\_ACTION\_SEND\_EMAIL**</dt> <dt>6</dt></span></span> </dl>       | <span data-ttu-id="3f932-119">Cette action envoie un message électronique.</span><span class="sxs-lookup"><span data-stu-id="3f932-119">This action sends an email message.</span></span><br/>                                                                                                                                                                                                       |
| <span id="TASK_ACTION_SHOW_MESSAGE"></span><span id="task_action_show_message"></span><dl> <span data-ttu-id="3f932-120"><dt>**Tâche \_ ACTION \_ afficher le \_ message**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="3f932-120"><dt>**TASK\_ACTION\_SHOW\_MESSAGE**</dt> <dt>7</dt></span></span> </dl> | <span data-ttu-id="3f932-121">Cette action affiche une boîte de message.</span><span class="sxs-lookup"><span data-stu-id="3f932-121">This action shows a message box.</span></span><br/>                                                                                                                                                                                                          |



 

## <a name="remarks"></a><span data-ttu-id="3f932-122">Notes</span><span class="sxs-lookup"><span data-stu-id="3f932-122">Remarks</span></span>

<span data-ttu-id="3f932-123">Le type d’action est défini lors de la création de l’action et ne peut pas être modifié ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="3f932-123">The action type is defined when the action is created and cannot be changed later.</span></span> <span data-ttu-id="3f932-124">Pour plus d’informations sur la création d’une action, consultez [**ActionCollection. Create**](actioncollection-create.md).</span><span class="sxs-lookup"><span data-stu-id="3f932-124">For information on creating an action, see [**ActionCollection.Create**](actioncollection-create.md).</span></span>

<span data-ttu-id="3f932-125">Pour plus d’informations sur la façon dont les actions et les tâches fonctionnent ensemble, consultez [actions des tâches](task-actions.md).</span><span class="sxs-lookup"><span data-stu-id="3f932-125">For information on how actions and tasks work together, see [Task Actions](task-actions.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3f932-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3f932-126">Requirements</span></span>



| <span data-ttu-id="3f932-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3f932-127">Requirement</span></span> | <span data-ttu-id="3f932-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="3f932-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3f932-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3f932-129">Minimum supported client</span></span><br/> | <span data-ttu-id="3f932-130">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3f932-130">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="3f932-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3f932-131">Minimum supported server</span></span><br/> | <span data-ttu-id="3f932-132">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3f932-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3f932-133">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="3f932-133">Type library</span></span><br/>             | <dl> <span data-ttu-id="3f932-134"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="3f932-134"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="3f932-135">DLL</span><span class="sxs-lookup"><span data-stu-id="3f932-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3f932-136"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3f932-136"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3f932-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3f932-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f932-138">**\_type d’action de tâche \_**</span><span class="sxs-lookup"><span data-stu-id="3f932-138">**TASK\_ACTION\_TYPE**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_action_type)
</dt> <dt>

[<span data-ttu-id="3f932-139">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="3f932-139">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="3f932-140">**Action**</span><span class="sxs-lookup"><span data-stu-id="3f932-140">**Action**</span></span>](action.md)
</dt> </dl>

 

 





