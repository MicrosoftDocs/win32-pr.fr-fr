---
title: ActionCollection. Create, méthode
description: Pour les scripts, crée et ajoute une nouvelle action à la collection.
ms.assetid: f33542e1-ee49-4696-b2ab-c48a9b5440d4
keywords:
- Créer une méthode Planificateur de tâches
- Create Method Planificateur de tâches, objet ActionCollection
- Planificateur de tâches d’objets ActionCollection, méthode Create
topic_type:
- apiref
api_name:
- ActionCollection.Create
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 50ec2ede228a27e753316860ac44e604d39e2e4b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508878"
---
# <a name="actioncollectioncreate-method"></a><span data-ttu-id="45955-106">ActionCollection. Create, méthode</span><span class="sxs-lookup"><span data-stu-id="45955-106">ActionCollection.Create method</span></span>

<span data-ttu-id="45955-107">Pour les scripts, crée et ajoute une nouvelle action à la collection.</span><span class="sxs-lookup"><span data-stu-id="45955-107">For scripting, creates and adds a new action to the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="45955-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="45955-108">Syntax</span></span>


```VB
ActionCollection.Create( _
  ByVal type _
)
```



## <a name="parameters"></a><span data-ttu-id="45955-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="45955-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="45955-110">*type* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="45955-110">*type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45955-111">Ce paramètre est défini sur l’une des constantes d’énumération de [**\_ \_ type d’action de tâche**](/windows/desktop/api/taskschd/ne-taskschd-task_action_type) suivantes.</span><span class="sxs-lookup"><span data-stu-id="45955-111">This parameter is set to one of the following [**TASK\_ACTION\_TYPE**](/windows/desktop/api/taskschd/ne-taskschd-task_action_type) enumeration constants.</span></span>



| <span data-ttu-id="45955-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="45955-112">Value</span></span>                                                                                                                                                                                                                                                   | <span data-ttu-id="45955-113">Signification</span><span class="sxs-lookup"><span data-stu-id="45955-113">Meaning</span></span>                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TASK_ACTION_EXEC"></span><span id="task_action_exec"></span><dl> <span data-ttu-id="45955-114"><dt>**Tâche \_ ACTION \_ Exec**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="45955-114"><dt>**TASK\_ACTION\_EXEC**</dt> <dt>0</dt></span></span> </dl>                          | <span data-ttu-id="45955-115">L’action effectue une opération de ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="45955-115">The action performs a command-line operation.</span></span> <span data-ttu-id="45955-116">Par exemple, l’action peut exécuter un script, lancer un exécutable ou, si le nom d’un document est fourni, Rechercher l’application associée et lancer l’application avec le document.</span><span class="sxs-lookup"><span data-stu-id="45955-116">For example, the action could run a script, launch an executable, or, if the name of a document is provided, find its associated application and launch the application with the document.</span></span><br/> |
| <span id="TASK_ACTION_COM_HANDLER"></span><span id="task_action_com_handler"></span><dl> <span data-ttu-id="45955-117"><dt>**Tâche \_ \_ \_ Gestionnaire com d’action**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="45955-117"><dt>**TASK\_ACTION\_COM\_HANDLER**</dt> <dt>5</dt></span></span> </dl>    | <span data-ttu-id="45955-118">L’action déclenche un gestionnaire.</span><span class="sxs-lookup"><span data-stu-id="45955-118">The action fires a handler.</span></span><br/>                                                                                                                                                                                                              |
| <span id="TASK_ACTION_SEND_EMAIL"></span><span id="task_action_send_email"></span><dl> <span data-ttu-id="45955-119"><dt>**Tâche \_ ACTION \_ Envoyer un \_ e-mail**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="45955-119"><dt>**TASK\_ACTION\_SEND\_EMAIL**</dt> <dt>6</dt></span></span> </dl>       | <span data-ttu-id="45955-120">Cette action envoie un message électronique.</span><span class="sxs-lookup"><span data-stu-id="45955-120">This action sends email message.</span></span><br/>                                                                                                                                                                                                         |
| <span id="TASK_ACTION_SHOW_MESSAGE"></span><span id="task_action_show_message"></span><dl> <span data-ttu-id="45955-121"><dt>**Tâche \_ ACTION \_ afficher le \_ message**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="45955-121"><dt>**TASK\_ACTION\_SHOW\_MESSAGE**</dt> <dt>7</dt></span></span> </dl> | <span data-ttu-id="45955-122">Cette action affiche une boîte de message.</span><span class="sxs-lookup"><span data-stu-id="45955-122">This action shows a message box.</span></span><br/>                                                                                                                                                                                                         |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="45955-123">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="45955-123">Return value</span></span>

<span data-ttu-id="45955-124">Objet d' [**action**](action.md) qui représente la nouvelle action.</span><span class="sxs-lookup"><span data-stu-id="45955-124">An [**Action**](action.md) object that represents the new action.</span></span>

## <a name="remarks"></a><span data-ttu-id="45955-125">Notes</span><span class="sxs-lookup"><span data-stu-id="45955-125">Remarks</span></span>

<span data-ttu-id="45955-126">Vous ne pouvez pas ajouter plus de 32 actions à la collection.</span><span class="sxs-lookup"><span data-stu-id="45955-126">You cannot add more than 32 actions to the collection.</span></span>

## <a name="requirements"></a><span data-ttu-id="45955-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="45955-127">Requirements</span></span>



| <span data-ttu-id="45955-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="45955-128">Requirement</span></span> | <span data-ttu-id="45955-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="45955-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="45955-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="45955-130">Minimum supported client</span></span><br/> | <span data-ttu-id="45955-131">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="45955-131">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="45955-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="45955-132">Minimum supported server</span></span><br/> | <span data-ttu-id="45955-133">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="45955-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="45955-134">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="45955-134">Type library</span></span><br/>             | <dl> <span data-ttu-id="45955-135"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="45955-135"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="45955-136">DLL</span><span class="sxs-lookup"><span data-stu-id="45955-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="45955-137"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="45955-137"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="45955-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="45955-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45955-139">**\_type d’action de tâche \_**</span><span class="sxs-lookup"><span data-stu-id="45955-139">**TASK\_ACTION\_TYPE**</span></span>](/windows/desktop/api/taskschd/ne-taskschd-task_action_type)
</dt> <dt>

[<span data-ttu-id="45955-140">Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="45955-140">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="45955-141">**ActionCollection**</span><span class="sxs-lookup"><span data-stu-id="45955-141">**ActionCollection**</span></span>](actioncollection.md)
</dt> <dt>

[<span data-ttu-id="45955-142">**Action**</span><span class="sxs-lookup"><span data-stu-id="45955-142">**Action**</span></span>](action.md)
</dt> <dt>

[<span data-ttu-id="45955-143">**ExecAction**</span><span class="sxs-lookup"><span data-stu-id="45955-143">**ExecAction**</span></span>](execaction.md)
</dt> <dt>

[<span data-ttu-id="45955-144">**EmailAction**</span><span class="sxs-lookup"><span data-stu-id="45955-144">**EmailAction**</span></span>](emailaction.md)
</dt> <dt>

[<span data-ttu-id="45955-145">**ShowMessageAction**</span><span class="sxs-lookup"><span data-stu-id="45955-145">**ShowMessageAction**</span></span>](showmessageaction.md)
</dt> <dt>

[<span data-ttu-id="45955-146">**ComHandlerAction**</span><span class="sxs-lookup"><span data-stu-id="45955-146">**ComHandlerAction**</span></span>](comhandleraction.md)
</dt> </dl>

 

 





