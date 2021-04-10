---
title: Objet ExecAction
description: Objet de script qui représente une action qui exécute une opération de ligne de commande.
ms.assetid: 51d2746d-3a90-4e8b-ac2b-d73193b3aa74
keywords:
- Planificateur de tâches d’exécution de l’action, interface
- Objet ExecAction Planificateur de tâches
- Planificateur de tâches d’objets ExecAction, Description
topic_type:
- apiref
api_name:
- ExecAction
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cddd1b9b44612b4ce896fb3ceb99a6deeaa5e3a1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105691"
---
# <a name="execaction-object"></a><span data-ttu-id="d1aa1-106">Objet ExecAction</span><span class="sxs-lookup"><span data-stu-id="d1aa1-106">ExecAction object</span></span>

<span data-ttu-id="d1aa1-107">Objet de script qui représente une action qui exécute une opération de ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="d1aa1-107">Scripting object that represents an action that executes a command-line operation.</span></span>

## <a name="members"></a><span data-ttu-id="d1aa1-108">Membres</span><span class="sxs-lookup"><span data-stu-id="d1aa1-108">Members</span></span>

<span data-ttu-id="d1aa1-109">L’objet **ExecAction** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="d1aa1-109">The **ExecAction** object has these types of members:</span></span>

-   [<span data-ttu-id="d1aa1-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d1aa1-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d1aa1-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="d1aa1-111">Properties</span></span>

<span data-ttu-id="d1aa1-112">L’objet **ExecAction** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="d1aa1-112">The **ExecAction** object has these properties.</span></span>



| <span data-ttu-id="d1aa1-113">Propriété</span><span class="sxs-lookup"><span data-stu-id="d1aa1-113">Property</span></span>                                                            | <span data-ttu-id="d1aa1-114">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="d1aa1-114">Access type</span></span>           | <span data-ttu-id="d1aa1-115">Description</span><span class="sxs-lookup"><span data-stu-id="d1aa1-115">Description</span></span>                                                                                                                       |
|:--------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d1aa1-116">**Arguments**</span><span class="sxs-lookup"><span data-stu-id="d1aa1-116">**Arguments**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_arguments)<br/>               | <span data-ttu-id="d1aa1-117">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="d1aa1-117">Read/write</span></span><br/> | <span data-ttu-id="d1aa1-118">Obtient ou définit les arguments associés à l’opération de ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="d1aa1-118">Gets or sets the arguments associated with the command-line operation.</span></span><br/>                                                 |
| [<span data-ttu-id="d1aa1-119">**Identifi**</span><span class="sxs-lookup"><span data-stu-id="d1aa1-119">**Id**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-iaction-get_id)<br/>                                 | <span data-ttu-id="d1aa1-120">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="d1aa1-120">Read/write</span></span><br/> | <span data-ttu-id="d1aa1-121">Hérité de l’objet d' [**action**](action.md) .</span><span class="sxs-lookup"><span data-stu-id="d1aa1-121">Inherited from the [**Action**](action.md) object.</span></span> <span data-ttu-id="d1aa1-122">Obtient ou définit l’identificateur de l’action.</span><span class="sxs-lookup"><span data-stu-id="d1aa1-122">Gets or sets the identifier of the action.</span></span><br/>                         |
| [<span data-ttu-id="d1aa1-123">**D**</span><span class="sxs-lookup"><span data-stu-id="d1aa1-123">**Path**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_path)<br/>                         | <span data-ttu-id="d1aa1-124">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="d1aa1-124">Read/write</span></span><br/> | <span data-ttu-id="d1aa1-125">Obtient ou définit le chemin d’accès à un fichier exécutable.</span><span class="sxs-lookup"><span data-stu-id="d1aa1-125">Gets or sets the path to an executable file.</span></span><br/>                                                                           |
| [<span data-ttu-id="d1aa1-126">**Entrer**</span><span class="sxs-lookup"><span data-stu-id="d1aa1-126">**Type**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-iaction-get_type)<br/>                             | <span data-ttu-id="d1aa1-127">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="d1aa1-127">Read-only</span></span><br/>  | <span data-ttu-id="d1aa1-128">Hérité de l’objet d' [**action**](action.md) .</span><span class="sxs-lookup"><span data-stu-id="d1aa1-128">Inherited from the [**Action**](action.md) object.</span></span> <span data-ttu-id="d1aa1-129">Obtient le type d'action.</span><span class="sxs-lookup"><span data-stu-id="d1aa1-129">Gets the type of the action.</span></span><br/>                                       |
| [<span data-ttu-id="d1aa1-130">**WorkingDirectory**</span><span class="sxs-lookup"><span data-stu-id="d1aa1-130">**WorkingDirectory**</span></span>](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_workingdirectory)<br/> | <span data-ttu-id="d1aa1-131">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="d1aa1-131">Read/write</span></span><br/> | <span data-ttu-id="d1aa1-132">Obtient ou définit le répertoire qui contient le fichier exécutable ou les fichiers utilisés par le fichier exécutable.</span><span class="sxs-lookup"><span data-stu-id="d1aa1-132">Gets or sets the directory that contains either the executable file or the files that are used by the executable file.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d1aa1-133">Notes</span><span class="sxs-lookup"><span data-stu-id="d1aa1-133">Remarks</span></span>

<span data-ttu-id="d1aa1-134">Si les variables d’environnement sont utilisées dans les propriétés [**path**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_path), [**arguments**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_arguments)ou [**WorkingDirectory**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_workingdirectory) , les valeurs des variables d’environnement sont mises en cache et utilisées lors du lancement du Taskeng.exe (le moteur de tâches).</span><span class="sxs-lookup"><span data-stu-id="d1aa1-134">If environment variables are used in the [**Path**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_path), [**Arguments**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_arguments), or [**WorkingDirectory**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_workingdirectory) properties, then the values of the environment variables are cached and used when the Taskeng.exe (the task engine) is launched.</span></span> <span data-ttu-id="d1aa1-135">Les modifications apportées aux variables d’environnement qui se produisent après le lancement du moteur de tâche ne sont pas utilisées par le moteur de tâche.</span><span class="sxs-lookup"><span data-stu-id="d1aa1-135">Changes to the environment variables that occur after the task engine is launched will not be used by the task engine.</span></span>

<span data-ttu-id="d1aa1-136">Cette action effectue une opération de ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="d1aa1-136">This action performs a command-line operation.</span></span> <span data-ttu-id="d1aa1-137">Par exemple, l’action peut exécuter un script ou lancer un exécutable.</span><span class="sxs-lookup"><span data-stu-id="d1aa1-137">For example, the action could run a script or launch an executable.</span></span>

<span data-ttu-id="d1aa1-138">Lors de la lecture ou de l’écriture de données XML, une action d’exécution est spécifiée dans l’élément [**Exec**](taskschedulerschema-exec-actiongroup-element.md) du schéma planificateur de tâches.</span><span class="sxs-lookup"><span data-stu-id="d1aa1-138">When reading or writing XML, an execution action is specified in the [**Exec**](taskschedulerschema-exec-actiongroup-element.md) element of the Task Scheduler schema.</span></span>

## <a name="examples"></a><span data-ttu-id="d1aa1-139">Exemples</span><span class="sxs-lookup"><span data-stu-id="d1aa1-139">Examples</span></span>

<span data-ttu-id="d1aa1-140">Pour plus d’informations et pour obtenir un exemple de code pour cet objet de script, consultez [exemple de déclenchement temporel (script)](time-trigger-example--scripting-.md).</span><span class="sxs-lookup"><span data-stu-id="d1aa1-140">For more information and example code for this scripting object, see [Time Trigger Example (Scripting)](time-trigger-example--scripting-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d1aa1-141">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d1aa1-141">Requirements</span></span>



| <span data-ttu-id="d1aa1-142">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d1aa1-142">Requirement</span></span> | <span data-ttu-id="d1aa1-143">Valeur</span><span class="sxs-lookup"><span data-stu-id="d1aa1-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d1aa1-144">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d1aa1-144">Minimum supported client</span></span><br/> | <span data-ttu-id="d1aa1-145">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d1aa1-145">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="d1aa1-146">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d1aa1-146">Minimum supported server</span></span><br/> | <span data-ttu-id="d1aa1-147">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d1aa1-147">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d1aa1-148">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="d1aa1-148">Type library</span></span><br/>             | <dl> <span data-ttu-id="d1aa1-149"><dt>Taskschd. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="d1aa1-149"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="d1aa1-150">DLL</span><span class="sxs-lookup"><span data-stu-id="d1aa1-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d1aa1-151"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d1aa1-151"><dt>Taskschd.dll</dt></span></span> </dl> |



 

 





