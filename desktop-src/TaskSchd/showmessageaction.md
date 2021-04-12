---
title: Objet ShowMessageAction
description: Pour les scripts, représente une action qui affiche une boîte de message lorsqu’une tâche est activée.
ms.assetid: fdd22eef-965c-4a81-954c-66011c435ab9
keywords:
- Objet ShowMessageAction Planificateur de tâches
- Planificateur de tâches d’objets ShowMessageAction, Description
topic_type:
- apiref
api_name:
- ShowMessageAction
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef1e500f0492ad010e88719a467fda38f85e184c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384231"
---
# <a name="showmessageaction-object"></a><span data-ttu-id="b7ccf-105">Objet ShowMessageAction</span><span class="sxs-lookup"><span data-stu-id="b7ccf-105">ShowMessageAction object</span></span>

<span data-ttu-id="b7ccf-106">\[Cet objet n’est plus pris en charge.</span><span class="sxs-lookup"><span data-stu-id="b7ccf-106">\[This object is no longer supported.</span></span> <span data-ttu-id="b7ccf-107">Vous pouvez utiliser IExecAction avec la fonction Windows Scripting [**MsgBox**](/previous-versions/sfw6660x(v=vs.80)) pour afficher un message dans la session utilisateur.\]</span><span class="sxs-lookup"><span data-stu-id="b7ccf-107">You can use IExecAction with the Windows scripting [**MsgBox function**](/previous-versions/sfw6660x(v=vs.80)) to show a message in the user session.\]</span></span>

<span data-ttu-id="b7ccf-108">Pour les scripts, représente une action qui affiche une boîte de message lorsqu’une tâche est activée.</span><span class="sxs-lookup"><span data-stu-id="b7ccf-108">For scripting, represents an action that shows a message box when a task is activated.</span></span>

## <a name="members"></a><span data-ttu-id="b7ccf-109">Membres</span><span class="sxs-lookup"><span data-stu-id="b7ccf-109">Members</span></span>

<span data-ttu-id="b7ccf-110">L’objet **ShowMessageAction** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="b7ccf-110">The **ShowMessageAction** object has these types of members:</span></span>

-   [<span data-ttu-id="b7ccf-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b7ccf-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b7ccf-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="b7ccf-112">Properties</span></span>

<span data-ttu-id="b7ccf-113">L’objet **ShowMessageAction** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="b7ccf-113">The **ShowMessageAction** object has these properties.</span></span>



| <span data-ttu-id="b7ccf-114">Propriété</span><span class="sxs-lookup"><span data-stu-id="b7ccf-114">Property</span></span>                                                        | <span data-ttu-id="b7ccf-115">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="b7ccf-115">Access type</span></span>           | <span data-ttu-id="b7ccf-116">Description</span><span class="sxs-lookup"><span data-stu-id="b7ccf-116">Description</span></span>                                                                                               |
|:----------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b7ccf-117">**Identifi**</span><span class="sxs-lookup"><span data-stu-id="b7ccf-117">**Id**</span></span>](action-id.md)<br/>                              | <span data-ttu-id="b7ccf-118">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b7ccf-118">Read/write</span></span><br/> | <span data-ttu-id="b7ccf-119">Hérité de l’objet d' [**action**](action.md) .</span><span class="sxs-lookup"><span data-stu-id="b7ccf-119">Inherited from the [**Action**](action.md) object.</span></span> <span data-ttu-id="b7ccf-120">Obtient ou définit l’identificateur de l’action.</span><span class="sxs-lookup"><span data-stu-id="b7ccf-120">Gets or sets the identifier of the action.</span></span><br/> |
| [<span data-ttu-id="b7ccf-121">**MessageBody**</span><span class="sxs-lookup"><span data-stu-id="b7ccf-121">**MessageBody**</span></span>](showmessageaction-messagebody.md)<br/> | <span data-ttu-id="b7ccf-122">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b7ccf-122">Read/write</span></span><br/> | <span data-ttu-id="b7ccf-123">Obtient ou définit le texte du message affiché dans le corps de la boîte de message.</span><span class="sxs-lookup"><span data-stu-id="b7ccf-123">Gets or sets the message text that is displayed in the body of the message box.</span></span><br/>                |
| [<span data-ttu-id="b7ccf-124">**Intitulé**</span><span class="sxs-lookup"><span data-stu-id="b7ccf-124">**Title**</span></span>](showmessageaction-title.md)<br/>             | <span data-ttu-id="b7ccf-125">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="b7ccf-125">Read/write</span></span><br/> | <span data-ttu-id="b7ccf-126">Obtient ou définit le titre de la boîte de message.</span><span class="sxs-lookup"><span data-stu-id="b7ccf-126">Gets or sets the title of the message box.</span></span><br/>                                                     |
| [<span data-ttu-id="b7ccf-127">**Entrer**</span><span class="sxs-lookup"><span data-stu-id="b7ccf-127">**Type**</span></span>](action-type.md)<br/>                          | <span data-ttu-id="b7ccf-128">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="b7ccf-128">Read-only</span></span><br/>  | <span data-ttu-id="b7ccf-129">Hérité de l’objet d' [**action**](action.md) .</span><span class="sxs-lookup"><span data-stu-id="b7ccf-129">Inherited from the [**Action**](action.md) object.</span></span> <span data-ttu-id="b7ccf-130">Obtient le type d'action.</span><span class="sxs-lookup"><span data-stu-id="b7ccf-130">Gets the type of the action.</span></span><br/>               |



 

## <a name="remarks"></a><span data-ttu-id="b7ccf-131">Notes</span><span class="sxs-lookup"><span data-stu-id="b7ccf-131">Remarks</span></span>

<span data-ttu-id="b7ccf-132">Pour une tâche, qui contient une action de MessageBox, la boîte de message s’affiche si la tâche est activée et que la tâche a un type de connexion interactive.</span><span class="sxs-lookup"><span data-stu-id="b7ccf-132">For a task, that contains a message box action, the message box will be displayed if the task is activated and the task has an interactive logon type.</span></span> <span data-ttu-id="b7ccf-133">Pour définir le type d’ouverture de session de la tâche sur interactif, spécifiez 3 (**\_ \_ \_ jeton interactif d’ouverture de session**) ou 4 (**\_ \_ groupe d’ouverture de session de tâche**) dans la propriété [**LogonType**](principal-logontype.md) du principal de la tâche, ou dans le paramètre *LogonType* de [**TaskFolder. RegisterTask**](taskfolder-registertask.md) ou [**TaskFolder. RegisterTaskDefinition**](taskfolder-registertaskdefinition.md).</span><span class="sxs-lookup"><span data-stu-id="b7ccf-133">To set the task logon type to interactive, specify 3 (**TASK\_LOGON\_INTERACTIVE\_TOKEN**) or 4 (**TASK\_LOGON\_GROUP**) in the [**LogonType**](principal-logontype.md) property of the task principal, or in the *logonType* parameter of [**TaskFolder.RegisterTask**](taskfolder-registertask.md) or [**TaskFolder.RegisterTaskDefinition**](taskfolder-registertaskdefinition.md).</span></span>

<span data-ttu-id="b7ccf-134">Lors de la lecture ou de l’écriture de votre propre code XML pour une tâche, une action de MessageBox est spécifiée à l’aide de l’élément [**ShowMessage**](taskschedulerschema-showmessage-actiongroup-element.md) du schéma planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="b7ccf-134">When reading or writing your own XML for a task, a message box action is specified using the [**ShowMessage**](taskschedulerschema-showmessage-actiongroup-element.md) element of the Task Scheduler schema.</span></span>

## <a name="examples"></a><span data-ttu-id="b7ccf-135">Exemples</span><span class="sxs-lookup"><span data-stu-id="b7ccf-135">Examples</span></span>

<span data-ttu-id="b7ccf-136">Pour plus d’informations et pour obtenir un exemple de code pour cet objet de script, consultez exemple de MessageBox [(script)](/previous-versions//aa381916(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="b7ccf-136">For more information and example code for this scripting object, see [Message Box Example (Scripting)](/previous-versions//aa381916(v=vs.85)).</span></span>

## <a name="requirements"></a><span data-ttu-id="b7ccf-137">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b7ccf-137">Requirements</span></span>



| <span data-ttu-id="b7ccf-138">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b7ccf-138">Requirement</span></span> | <span data-ttu-id="b7ccf-139">Valeur</span><span class="sxs-lookup"><span data-stu-id="b7ccf-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b7ccf-140">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b7ccf-140">Minimum supported client</span></span><br/> | <span data-ttu-id="b7ccf-141">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b7ccf-141">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="b7ccf-142">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b7ccf-142">Minimum supported server</span></span><br/> | <span data-ttu-id="b7ccf-143">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b7ccf-143">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b7ccf-144">Fin de la prise en charge des clients</span><span class="sxs-lookup"><span data-stu-id="b7ccf-144">End of client support</span></span><br/>    | <span data-ttu-id="b7ccf-145">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b7ccf-145">Windows 7</span></span><br/>                                                                    |
| <span data-ttu-id="b7ccf-146">Fin de la prise en charge des serveurs</span><span class="sxs-lookup"><span data-stu-id="b7ccf-146">End of server support</span></span><br/>    | <span data-ttu-id="b7ccf-147">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b7ccf-147">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="b7ccf-148">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="b7ccf-148">Type library</span></span><br/>             | <dl> <span data-ttu-id="b7ccf-149"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="b7ccf-149"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="b7ccf-150">DLL</span><span class="sxs-lookup"><span data-stu-id="b7ccf-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b7ccf-151"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b7ccf-151"><dt>Taskschd.dll</dt></span></span> </dl> |



 

