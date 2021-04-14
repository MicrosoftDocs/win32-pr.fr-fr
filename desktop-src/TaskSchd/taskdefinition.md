---
title: Objet TaskDefinition
description: Objet de script qui définit tous les composants d’une tâche, tels que les paramètres de tâche, les déclencheurs, les actions et les informations d’inscription.
ms.assetid: d5887024-21af-40cf-a97d-f695f60394d9
keywords:
- Objet TaskDefinition Planificateur de tâches
- Planificateur de tâches d’objets TaskDefinition, Description
topic_type:
- apiref
api_name:
- TaskDefinition
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42d911218f64b386c08091f981903126f7506e3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508774"
---
# <a name="taskdefinition-object"></a><span data-ttu-id="7b45a-105">Objet TaskDefinition</span><span class="sxs-lookup"><span data-stu-id="7b45a-105">TaskDefinition object</span></span>

<span data-ttu-id="7b45a-106">Objet de script qui définit tous les composants d’une tâche, tels que les paramètres de tâche, les déclencheurs, les actions et les informations d’inscription.</span><span class="sxs-lookup"><span data-stu-id="7b45a-106">Scripting object that defines all the components of a task, such as the task settings, triggers, actions, and registration information.</span></span>

## <a name="members"></a><span data-ttu-id="7b45a-107">Membres</span><span class="sxs-lookup"><span data-stu-id="7b45a-107">Members</span></span>

<span data-ttu-id="7b45a-108">L’objet **TaskDefinition** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="7b45a-108">The **TaskDefinition** object has these types of members:</span></span>

-   [<span data-ttu-id="7b45a-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="7b45a-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7b45a-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="7b45a-110">Properties</span></span>

<span data-ttu-id="7b45a-111">L’objet **TaskDefinition** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="7b45a-111">The **TaskDefinition** object has these properties.</span></span>



| <span data-ttu-id="7b45a-112">Propriété</span><span class="sxs-lookup"><span data-stu-id="7b45a-112">Property</span></span>                                                               | <span data-ttu-id="7b45a-113">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="7b45a-113">Access type</span></span>           | <span data-ttu-id="7b45a-114">Description</span><span class="sxs-lookup"><span data-stu-id="7b45a-114">Description</span></span>                                                                                                                                                                             |
|:-----------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7b45a-115">**Actions**</span><span class="sxs-lookup"><span data-stu-id="7b45a-115">**Actions**</span></span>](taskdefinition-actions.md)<br/>                   | <span data-ttu-id="7b45a-116">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="7b45a-116">Read/write</span></span><br/> | <span data-ttu-id="7b45a-117">Obtient ou définit une collection d’actions exécutées par la tâche.</span><span class="sxs-lookup"><span data-stu-id="7b45a-117">Gets or sets a collection of actions that are performed by the task.</span></span><br/>                                                                                                         |
| [<span data-ttu-id="7b45a-118">**Données**</span><span class="sxs-lookup"><span data-stu-id="7b45a-118">**Data**</span></span>](taskdefinition-data.md)<br/>                         | <span data-ttu-id="7b45a-119">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="7b45a-119">Read/write</span></span><br/> | <span data-ttu-id="7b45a-120">Obtient ou définit les données associées à la tâche.</span><span class="sxs-lookup"><span data-stu-id="7b45a-120">Gets or sets the data that is associated with the task.</span></span> <span data-ttu-id="7b45a-121">Ces données sont ignorées par le service Planificateur de tâches, mais elles sont utilisées par des tiers qui souhaitent étendre le format des tâches.</span><span class="sxs-lookup"><span data-stu-id="7b45a-121">This data is ignored by the Task Scheduler service, but is used by third-parties who wish to extend the task format.</span></span><br/> |
| [<span data-ttu-id="7b45a-122">**Directeur**</span><span class="sxs-lookup"><span data-stu-id="7b45a-122">**Principal**</span></span>](taskdefinition-principal.md)<br/>               | <span data-ttu-id="7b45a-123">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="7b45a-123">Read/write</span></span><br/> | <span data-ttu-id="7b45a-124">Obtient ou définit le principal de la tâche qui fournit les informations d’identification de sécurité pour la tâche.</span><span class="sxs-lookup"><span data-stu-id="7b45a-124">Gets or sets the principal for the task that provides the security credentials for the task.</span></span><br/>                                                                                 |
| [<span data-ttu-id="7b45a-125">**RegistrationInfo**</span><span class="sxs-lookup"><span data-stu-id="7b45a-125">**RegistrationInfo**</span></span>](taskdefinition-registrationinfo.md)<br/> | <span data-ttu-id="7b45a-126">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="7b45a-126">Read/write</span></span><br/> | <span data-ttu-id="7b45a-127">Obtient ou définit les informations d’inscription utilisées pour décrire une tâche, telles que la description de la tâche, l’auteur de la tâche et la date à laquelle la tâche est inscrite.</span><span class="sxs-lookup"><span data-stu-id="7b45a-127">Gets or sets the registration information that is used to describe a task, such as the description of the task, the author of the task, and the date the task is registered.</span></span><br/> |
| [<span data-ttu-id="7b45a-128">**Paramètres**</span><span class="sxs-lookup"><span data-stu-id="7b45a-128">**Settings**</span></span>](taskdefinition-settings.md)<br/>                 | <span data-ttu-id="7b45a-129">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="7b45a-129">Read/write</span></span><br/> | <span data-ttu-id="7b45a-130">Obtient ou définit les paramètres qui définissent la façon dont le service de Planificateur de tâches exécute la tâche.</span><span class="sxs-lookup"><span data-stu-id="7b45a-130">Gets or sets the settings that define how the Task Scheduler service performs the task.</span></span><br/>                                                                                      |
| [<span data-ttu-id="7b45a-131">**Déclencheurs**</span><span class="sxs-lookup"><span data-stu-id="7b45a-131">**Triggers**</span></span>](taskdefinition-triggers.md)<br/>                 | <span data-ttu-id="7b45a-132">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="7b45a-132">Read/write</span></span><br/> | <span data-ttu-id="7b45a-133">Obtient ou définit une collection de déclencheurs utilisés pour démarrer une tâche.</span><span class="sxs-lookup"><span data-stu-id="7b45a-133">Gets or sets a collection of triggers that are used to start a task.</span></span><br/>                                                                                                         |
| [<span data-ttu-id="7b45a-134">**XmlText**</span><span class="sxs-lookup"><span data-stu-id="7b45a-134">**XmlText**</span></span>](taskdefinition-xmltext.md)<br/>                   | <span data-ttu-id="7b45a-135">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="7b45a-135">Read/write</span></span><br/> | <span data-ttu-id="7b45a-136">Obtient ou définit la définition XML de la tâche.</span><span class="sxs-lookup"><span data-stu-id="7b45a-136">Gets or sets the XML-formatted definition of the task.</span></span><br/>                                                                                                                       |



 

## <a name="remarks"></a><span data-ttu-id="7b45a-137">Notes</span><span class="sxs-lookup"><span data-stu-id="7b45a-137">Remarks</span></span>

<span data-ttu-id="7b45a-138">Lors de la lecture ou de l’écriture de votre propre code XML pour une tâche, une définition de tâche est spécifiée à l’aide de l’élément [**Task**](taskschedulerschema-task-element.md) du schéma planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="7b45a-138">When reading or writing your own XML for a task, a task definition is specified using the [**Task**](taskschedulerschema-task-element.md) element of the Task Scheduler schema.</span></span>

## <a name="examples"></a><span data-ttu-id="7b45a-139">Exemples</span><span class="sxs-lookup"><span data-stu-id="7b45a-139">Examples</span></span>

<span data-ttu-id="7b45a-140">Pour plus d’informations et pour obtenir un exemple de code pour cet objet de script, consultez [exemple de déclenchement temporel (script)](time-trigger-example--scripting-.md) , [exemple de déclenchement d’événements (script)](https://www.bing.com/search?q=Event+Trigger+Example+(Scripting)), exemple de [déclencheur quotidien (script)](daily-trigger-example--scripting-.md), [exemple de déclencheur d’inscription (](registration-trigger-example--scripting-.md)script), exemple de [déclencheur hebdomadaire (](weekly-trigger-example--scripting-.md)script), exemple de [déclencheur LOGON (script)](logon-trigger-example--scripting-.md)ou [exemple de déclencheur de démarrage](boot-trigger-example--scripting-.md)</span><span class="sxs-lookup"><span data-stu-id="7b45a-140">For more information and example code for this scripting object, see [Time Trigger Example (Scripting)](time-trigger-example--scripting-.md) , [Event Trigger Example (Scripting)](https://www.bing.com/search?q=Event+Trigger+Example+(Scripting)), [Daily Trigger Example (Scripting)](daily-trigger-example--scripting-.md), [Registration Trigger Example (Scripting)](registration-trigger-example--scripting-.md), [Weekly Trigger Example (Scripting)](weekly-trigger-example--scripting-.md), [Logon Trigger Example (Scripting)](logon-trigger-example--scripting-.md), or [Boot Trigger Example (Scripting)](boot-trigger-example--scripting-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7b45a-141">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7b45a-141">Requirements</span></span>



| <span data-ttu-id="7b45a-142">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7b45a-142">Requirement</span></span> | <span data-ttu-id="7b45a-143">Valeur</span><span class="sxs-lookup"><span data-stu-id="7b45a-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7b45a-144">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7b45a-144">Minimum supported client</span></span><br/> | <span data-ttu-id="7b45a-145">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7b45a-145">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="7b45a-146">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7b45a-146">Minimum supported server</span></span><br/> | <span data-ttu-id="7b45a-147">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7b45a-147">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="7b45a-148">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="7b45a-148">Type library</span></span><br/>             | <dl> <span data-ttu-id="7b45a-149"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="7b45a-149"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="7b45a-150">DLL</span><span class="sxs-lookup"><span data-stu-id="7b45a-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7b45a-151"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7b45a-151"><dt>Taskschd.dll</dt></span></span> </dl> |



 

 





