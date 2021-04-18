---
title: Élément exec (actionGroup)
description: Spécifie une action qui exécute une opération de ligne de commande.
ms.assetid: 84bdd1ec-4279-4282-b44a-4b5ad30503eb
keywords:
- Élément exec Planificateur de tâches
topic_type:
- apiref
api_name:
- Exec
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b29ba66be8f2d3aefaec4f437359f2af5275d2f0
ms.sourcegitcommit: 628fda3e63fd1d513ce9a5f55be8bbc4af4b2a4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "106523113"
---
# <a name="exec-actiongroup-element"></a><span data-ttu-id="0b711-104">Élément exec (actionGroup)</span><span class="sxs-lookup"><span data-stu-id="0b711-104">Exec (actionGroup) Element</span></span>

<span data-ttu-id="0b711-105">Spécifie une action qui exécute une opération de ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="0b711-105">Specifies an action that executes a command-line operation.</span></span>

``` syntax
<xs:element name="Exec"
    type="execType"
 />
```

<span data-ttu-id="0b711-106">L’élément **Exec** est défini par [**actionGroup**](taskschedulerschema-actiongroup-group.md) .</span><span class="sxs-lookup"><span data-stu-id="0b711-106">The **Exec** element is defined by the [**actionGroup**](taskschedulerschema-actiongroup-group.md) .</span></span>

## <a name="parent-element"></a><span data-ttu-id="0b711-107">Élément parent</span><span class="sxs-lookup"><span data-stu-id="0b711-107">Parent element</span></span>



| <span data-ttu-id="0b711-108">Élément</span><span class="sxs-lookup"><span data-stu-id="0b711-108">Element</span></span>                                                         | <span data-ttu-id="0b711-109">Dérivé de</span><span class="sxs-lookup"><span data-stu-id="0b711-109">Derived from</span></span>                                                       | <span data-ttu-id="0b711-110">Description</span><span class="sxs-lookup"><span data-stu-id="0b711-110">Description</span></span>                                            |
|-----------------------------------------------------------------|--------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="0b711-111">**Actions**</span><span class="sxs-lookup"><span data-stu-id="0b711-111">**Actions**</span></span>](taskschedulerschema-actions-tasktype-element.md) | [<span data-ttu-id="0b711-112">**actionsType**</span><span class="sxs-lookup"><span data-stu-id="0b711-112">**actionsType**</span></span>](taskschedulerschema-actionstype-complextype.md) | <span data-ttu-id="0b711-113">Contient les actions effectuées par la tâche.</span><span class="sxs-lookup"><span data-stu-id="0b711-113">Contains the actions performed by the task.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="0b711-114">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="0b711-114">Child elements</span></span>



| <span data-ttu-id="0b711-115">Élément</span><span class="sxs-lookup"><span data-stu-id="0b711-115">Element</span></span>                                                                           | <span data-ttu-id="0b711-116">Type</span><span class="sxs-lookup"><span data-stu-id="0b711-116">Type</span></span>       | <span data-ttu-id="0b711-117">Description</span><span class="sxs-lookup"><span data-stu-id="0b711-117">Description</span></span>                                                                                                  |
|-----------------------------------------------------------------------------------|------------|--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0b711-118">**Arguments**</span><span class="sxs-lookup"><span data-stu-id="0b711-118">**Arguments**</span></span>](taskschedulerschema-arguments-exectype-element.md)               | <span data-ttu-id="0b711-119">**string**</span><span class="sxs-lookup"><span data-stu-id="0b711-119">**string**</span></span> | <span data-ttu-id="0b711-120">Spécifie les arguments associés à l’opération de ligne de commande.</span><span class="sxs-lookup"><span data-stu-id="0b711-120">Specifies the arguments associated with the command-line operation.</span></span><br/>                               |
| [<span data-ttu-id="0b711-121">**Commande**</span><span class="sxs-lookup"><span data-stu-id="0b711-121">**Command**</span></span>](taskschedulerschema-command-exectype-element.md)                   | <span data-ttu-id="0b711-122">**string**</span><span class="sxs-lookup"><span data-stu-id="0b711-122">**string**</span></span> | <span data-ttu-id="0b711-123">Spécifie le fichier exécutable ou le document à exécuter.</span><span class="sxs-lookup"><span data-stu-id="0b711-123">Specifies the executable file or document to be run.</span></span><br/>                                              |
| [<span data-ttu-id="0b711-124">**WorkingDirectory**</span><span class="sxs-lookup"><span data-stu-id="0b711-124">**WorkingDirectory**</span></span>](taskschedulerschema-workingdirectory-exectype-element.md) | <span data-ttu-id="0b711-125">string</span><span class="sxs-lookup"><span data-stu-id="0b711-125">string</span></span>     | <span data-ttu-id="0b711-126">Spécifie le répertoire dans lequel le fichier exécutable ou les fichiers utilisés par l’exécutable existent.</span><span class="sxs-lookup"><span data-stu-id="0b711-126">Specifies the directory where either the executable or those files used by the executable exists.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="0b711-127">Attributs</span><span class="sxs-lookup"><span data-stu-id="0b711-127">Attributes</span></span>



| <span data-ttu-id="0b711-128">Nom</span><span class="sxs-lookup"><span data-stu-id="0b711-128">Name</span></span> | <span data-ttu-id="0b711-129">Type</span><span class="sxs-lookup"><span data-stu-id="0b711-129">Type</span></span>       | <span data-ttu-id="0b711-130">Description</span><span class="sxs-lookup"><span data-stu-id="0b711-130">Description</span></span>                                                    |
|------|------------|----------------------------------------------------------------|
| <span data-ttu-id="0b711-131">id</span><span class="sxs-lookup"><span data-stu-id="0b711-131">id</span></span>   | <span data-ttu-id="0b711-132">**string**</span><span class="sxs-lookup"><span data-stu-id="0b711-132">**string**</span></span> | <span data-ttu-id="0b711-133">Identificateur de l’action exécutée par la tâche.</span><span class="sxs-lookup"><span data-stu-id="0b711-133">The identifier of the action performed by the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="0b711-134">Notes</span><span class="sxs-lookup"><span data-stu-id="0b711-134">Remarks</span></span>

<span data-ttu-id="0b711-135">Les éléments enfants répertoriés ci-dessus sont définis par le type complexe [**execType**](taskschedulerschema-exectype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="0b711-135">The child elements listed above are defined by the [**execType**](taskschedulerschema-exectype-complextype.md) complex type.</span></span>

<span data-ttu-id="0b711-136">Pour le développement de scripts, une action d’exécution est définie par l’objet [**ExecAction**](execaction.md) .</span><span class="sxs-lookup"><span data-stu-id="0b711-136">For script development, an execution action is defined by the [**ExecAction**](execaction.md) object.</span></span>

<span data-ttu-id="0b711-137">Pour le développement C++, une action d’exécution est définie par l’interface [**IExecAction**](/windows/desktop/api/taskschd/nn-taskschd-iexecaction) .</span><span class="sxs-lookup"><span data-stu-id="0b711-137">For C++ development, an execution action is defined by the [**IExecAction**](/windows/desktop/api/taskschd/nn-taskschd-iexecaction) interface.</span></span>

<span data-ttu-id="0b711-138">Si les variables d’environnement sont utilisées dans les éléments [**Command**](taskschedulerschema-command-exectype-element.md), [**arguments**](taskschedulerschema-arguments-exectype-element.md)ou [**WorkingDirectory**](taskschedulerschema-workingdirectory-exectype-element.md) , les valeurs des variables d’environnement sont mises en cache et utilisées lors du lancement du Taskeng.exe (le moteur de tâches).</span><span class="sxs-lookup"><span data-stu-id="0b711-138">If environment variables are used in the [**Command**](taskschedulerschema-command-exectype-element.md), [**Arguments**](taskschedulerschema-arguments-exectype-element.md), or [**WorkingDirectory**](taskschedulerschema-workingdirectory-exectype-element.md) elements, then the values of the environment variables are cached and used when the Taskeng.exe (the task engine) is launched.</span></span> <span data-ttu-id="0b711-139">Les modifications apportées aux variables d’environnement qui se produisent après le lancement du moteur de tâche ne sont pas utilisées par le moteur de tâche.</span><span class="sxs-lookup"><span data-stu-id="0b711-139">Changes to the environment variables that occur after the task engine is launched will not be used by the task engine.</span></span>

## <a name="examples"></a><span data-ttu-id="0b711-140">Exemples</span><span class="sxs-lookup"><span data-stu-id="0b711-140">Examples</span></span>

<span data-ttu-id="0b711-141">Pour obtenir un exemple complet du code XML d’une tâche qui utilise un déclencheur d’événement, consultez [exemple de déclencheur d’heure (XML)](time-trigger-example--xml-.md).</span><span class="sxs-lookup"><span data-stu-id="0b711-141">For a complete example of the XML for a task that uses an event trigger, see [Time Trigger Example (XML)](time-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0b711-142">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0b711-142">Requirements</span></span>



| <span data-ttu-id="0b711-143">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0b711-143">Requirement</span></span> | <span data-ttu-id="0b711-144">Valeur</span><span class="sxs-lookup"><span data-stu-id="0b711-144">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="0b711-145">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0b711-145">Minimum supported client</span></span><br/> | <span data-ttu-id="0b711-146">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0b711-146">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="0b711-147">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0b711-147">Minimum supported server</span></span><br/> | <span data-ttu-id="0b711-148">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0b711-148">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0b711-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0b711-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b711-150">Éléments de schéma Planificateur de tâches</span><span class="sxs-lookup"><span data-stu-id="0b711-150">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





