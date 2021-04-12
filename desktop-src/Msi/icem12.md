---
description: ICEM12 vérifie que dans une table ModuleSequence, les actions standard ont des numéros de séquence et les actions personnalisées ont des valeurs BaseAction et after.
ms.assetid: 1a168629-9865-4412-8317-8af8b9a7b8bd
title: ICEM12
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b37cbff2e29a85dd50ef1f044a43fdb8e48ffdd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034122"
---
# <a name="icem12"></a><span data-ttu-id="dc646-103">ICEM12</span><span class="sxs-lookup"><span data-stu-id="dc646-103">ICEM12</span></span>

<span data-ttu-id="dc646-104">ICEM12 vérifie que dans une table ModuleSequence, les actions standard ont des numéros de séquence et les actions personnalisées ont des valeurs BaseAction et after.</span><span class="sxs-lookup"><span data-stu-id="dc646-104">ICEM12 verifies that in a ModuleSequence table, standard actions have sequence numbers and custom actions have BaseAction and After values.</span></span>

<span data-ttu-id="dc646-105">Ce ICEM est disponible dans le fichier Mergemod. CUB fourni dans le kit de développement logiciel (SDK) Windows Installer 2,0 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="dc646-105">This ICEM is available in the Mergemod.cub file provided in the Windows Installer 2.0 SDK and later.</span></span> <span data-ttu-id="dc646-106">Pour plus d’informations, consultez [SDK Windows Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span><span class="sxs-lookup"><span data-stu-id="dc646-106">For details, see [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span>

## <a name="result"></a><span data-ttu-id="dc646-107">Résultats</span><span class="sxs-lookup"><span data-stu-id="dc646-107">Result</span></span>

<span data-ttu-id="dc646-108">ICEM12 publie une erreur dans les cas suivants :</span><span class="sxs-lookup"><span data-stu-id="dc646-108">ICEM12 posts an error in the following cases:</span></span>

-   <span data-ttu-id="dc646-109">Il trouve que le module contient une [action standard](standard-actions.md) sans numéro de séquence.</span><span class="sxs-lookup"><span data-stu-id="dc646-109">It finds the module contains a [standard action](standard-actions.md) without a sequence number.</span></span>
-   <span data-ttu-id="dc646-110">Elle constate qu’une action standard a des valeurs entrées dans les champs BaseAction ou after de la table [ModuleAdminUISequence](moduleadminuisequence-table.md), de la table [ModuleAdminExecuteSequence](moduleadminexecutesequence-table.md), de la table [ModuleAdvtExecuteSequence](moduleadvtexecutesequence-table.md), de la [table ModuleInstallUISequence](moduleinstalluisequence-table.md)ou de la [table ModuleInstallExecuteSequence](moduleinstallexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="dc646-110">It finds that a standard action has values entered in the BaseAction or After fields of the [ModuleAdminUISequence table](moduleadminuisequence-table.md), [ModuleAdminExecuteSequence table](moduleadminexecutesequence-table.md), [ModuleAdvtExecuteSequence table](moduleadvtexecutesequence-table.md), [ModuleInstallUISequence table](moduleinstalluisequence-table.md), or [ModuleInstallExecuteSequence table](moduleinstallexecutesequence-table.md).</span></span>
-   <span data-ttu-id="dc646-111">Il trouve que le module contient une [action personnalisée](custom-actions.md) sans aucune valeur entrée dans les champs Sequence, BaseAction ou after de la table [ModuleAdminUISequence](moduleadminuisequence-table.md), de la table [ModuleAdminExecuteSequence](moduleadminexecutesequence-table.md), de la table [ModuleAdvtExecuteSequence](moduleadvtexecutesequence-table.md), de la [table ModuleInstallUISequence](moduleinstalluisequence-table.md)ou de la [table ModuleInstallExecuteSequence](moduleinstallexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="dc646-111">It finds the module contains a [custom action](custom-actions.md) without any values entered into the Sequence, BaseAction or After fields of the [ModuleAdminUISequence table](moduleadminuisequence-table.md), [ModuleAdminExecuteSequence table](moduleadminexecutesequence-table.md), [ModuleAdvtExecuteSequence table](moduleadvtexecutesequence-table.md), [ModuleInstallUISequence table](moduleinstalluisequence-table.md), or [ModuleInstallExecuteSequence table](moduleinstallexecutesequence-table.md).</span></span>

<span data-ttu-id="dc646-112">ICEM12 publie un avertissement s’il trouve une action personnalisée qui a un numéro de séquence spécifié, mais aucune valeur dans les champs BaseAction ou after.</span><span class="sxs-lookup"><span data-stu-id="dc646-112">ICEM12 posts a warning if it finds a custom action that has a Sequence number specified, but no value in the BaseAction or After fields.</span></span>

<span data-ttu-id="dc646-113">Notez que toutes les actions trouvées dans la [table CustomAction](customaction-table.md) sont considérées comme des actions personnalisées.</span><span class="sxs-lookup"><span data-stu-id="dc646-113">Note that all actions found in the [CustomAction table](customaction-table.md) are considered custom actions.</span></span> <span data-ttu-id="dc646-114">Toutes les autres actions sont considérées comme des actions standard.</span><span class="sxs-lookup"><span data-stu-id="dc646-114">All other action are considered standard actions.</span></span>

## <a name="example"></a><span data-ttu-id="dc646-115">Exemple</span><span class="sxs-lookup"><span data-stu-id="dc646-115">Example</span></span>

<span data-ttu-id="dc646-116">ICEM12 publie les messages d’erreur et d’avertissement suivants pour un module qui contient les entrées de la base de données, comme indiqué ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="dc646-116">ICEM12 posts the following error and warning messages for a module that contains the database entries shown below:</span></span>

``` syntax
Error. Custom actions should use the BaseAction and After fields and not use the 
Sequence field in the Module Sequence tables. The custom action 'Action1' uses the Sequence field 
and does not use the BaseAction and After fields in the ModuleInstallExecuteSequence table. 
    
Error. Custom actions should not leave the Sequence, BaseAction, and After fields 
of the Module Sequence tables all empty. The custom action 'Action3' leaves the Sequence, 
BaseAction, and After fields empty in the ModuleAdminExecuteSequence table.

Error. Standard actions should not use the BaseAction and After fields in Module 
Sequence tables. The standard action 'Action2' has a values entered in the BaseAction 
or After fields of the ModuleAdminExecuteSequence table.

Error. Standard actions must have a entry in the Sequence field of Module Sequence 
tables. The standard action 'Action2' does not have a Sequence value in the 
ModuleExecuteSequence table.
```

[<span data-ttu-id="dc646-117">CustomAction</span><span class="sxs-lookup"><span data-stu-id="dc646-117">CustomAction</span></span>](customaction-table.md)



| <span data-ttu-id="dc646-118">Action</span><span class="sxs-lookup"><span data-stu-id="dc646-118">Action</span></span>  | <span data-ttu-id="dc646-119">Type</span><span class="sxs-lookup"><span data-stu-id="dc646-119">Type</span></span> | <span data-ttu-id="dc646-120">Source</span><span class="sxs-lookup"><span data-stu-id="dc646-120">Source</span></span>  | <span data-ttu-id="dc646-121">Cible</span><span class="sxs-lookup"><span data-stu-id="dc646-121">Target</span></span>  |
|---------|------|---------|---------|
| <span data-ttu-id="dc646-122">Action1</span><span class="sxs-lookup"><span data-stu-id="dc646-122">Action1</span></span> | <span data-ttu-id="dc646-123">30</span><span class="sxs-lookup"><span data-stu-id="dc646-123">30</span></span>   | <span data-ttu-id="dc646-124">source1</span><span class="sxs-lookup"><span data-stu-id="dc646-124">source1</span></span> | <span data-ttu-id="dc646-125">target1</span><span class="sxs-lookup"><span data-stu-id="dc646-125">target1</span></span> |
| <span data-ttu-id="dc646-126">Action3</span><span class="sxs-lookup"><span data-stu-id="dc646-126">Action3</span></span> | <span data-ttu-id="dc646-127">30</span><span class="sxs-lookup"><span data-stu-id="dc646-127">30</span></span>   | <span data-ttu-id="dc646-128">source3</span><span class="sxs-lookup"><span data-stu-id="dc646-128">source3</span></span> | <span data-ttu-id="dc646-129">target3</span><span class="sxs-lookup"><span data-stu-id="dc646-129">target3</span></span> |



 

[<span data-ttu-id="dc646-130">ModuleAdminExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="dc646-130">ModuleAdminExecuteSequence</span></span>](moduleadminexecutesequence-table.md)



| <span data-ttu-id="dc646-131">Action</span><span class="sxs-lookup"><span data-stu-id="dc646-131">Action</span></span>  | <span data-ttu-id="dc646-132">Séquence</span><span class="sxs-lookup"><span data-stu-id="dc646-132">Sequence</span></span> | <span data-ttu-id="dc646-133">BaseAction</span><span class="sxs-lookup"><span data-stu-id="dc646-133">BaseAction</span></span> | <span data-ttu-id="dc646-134">After</span><span class="sxs-lookup"><span data-stu-id="dc646-134">After</span></span> | <span data-ttu-id="dc646-135">Condition</span><span class="sxs-lookup"><span data-stu-id="dc646-135">Condition</span></span> |
|---------|----------|------------|-------|-----------|
| <span data-ttu-id="dc646-136">Action2</span><span class="sxs-lookup"><span data-stu-id="dc646-136">Action2</span></span> |          | <span data-ttu-id="dc646-137">Action1</span><span class="sxs-lookup"><span data-stu-id="dc646-137">Action1</span></span>    | <span data-ttu-id="dc646-138">1</span><span class="sxs-lookup"><span data-stu-id="dc646-138">1</span></span>     | <span data-ttu-id="dc646-139">true</span><span class="sxs-lookup"><span data-stu-id="dc646-139">true</span></span>      |
| <span data-ttu-id="dc646-140">Action3</span><span class="sxs-lookup"><span data-stu-id="dc646-140">Action3</span></span> |          |            |       | <span data-ttu-id="dc646-141">true</span><span class="sxs-lookup"><span data-stu-id="dc646-141">true</span></span>      |



 

[<span data-ttu-id="dc646-142">ModuleInstallExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="dc646-142">ModuleInstallExecuteSequence</span></span>](moduleinstallexecutesequence-table.md)



| <span data-ttu-id="dc646-143">Action</span><span class="sxs-lookup"><span data-stu-id="dc646-143">Action</span></span>  | <span data-ttu-id="dc646-144">Séquence</span><span class="sxs-lookup"><span data-stu-id="dc646-144">Sequence</span></span> | <span data-ttu-id="dc646-145">BaseAction</span><span class="sxs-lookup"><span data-stu-id="dc646-145">BaseAction</span></span> | <span data-ttu-id="dc646-146">After</span><span class="sxs-lookup"><span data-stu-id="dc646-146">After</span></span> | <span data-ttu-id="dc646-147">Condition</span><span class="sxs-lookup"><span data-stu-id="dc646-147">Condition</span></span> |
|---------|----------|------------|-------|-----------|
| <span data-ttu-id="dc646-148">Action1</span><span class="sxs-lookup"><span data-stu-id="dc646-148">Action1</span></span> | <span data-ttu-id="dc646-149">1</span><span class="sxs-lookup"><span data-stu-id="dc646-149">1</span></span>        |            |       | <span data-ttu-id="dc646-150">true</span><span class="sxs-lookup"><span data-stu-id="dc646-150">true</span></span>      |



 

<span data-ttu-id="dc646-151">Pour corriger ces erreurs, essayez ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="dc646-151">To fix these errors try the following:</span></span>

-   <span data-ttu-id="dc646-152">Supprimez le numéro de séquence de l’action personnalisée action1 et utilisez à la place les champs BaseAction et after.</span><span class="sxs-lookup"><span data-stu-id="dc646-152">Remove the sequence number for the custom action Action1 and use the BaseAction and After fields instead.</span></span>
-   <span data-ttu-id="dc646-153">Entrez les valeurs dans les champs Sequence, BaseAction ou after pour l’action personnalisée Action3.</span><span class="sxs-lookup"><span data-stu-id="dc646-153">Enter values into the Sequence, BaseAction, or After fields for the custom action Action3.</span></span> <span data-ttu-id="dc646-154">Laissez les champs BaseAction et after vides pour l’action standard action2.</span><span class="sxs-lookup"><span data-stu-id="dc646-154">Leave the BaseAction and After fields empty for standard action Action2.</span></span>
-   <span data-ttu-id="dc646-155">Ne laissez pas le champ séquence vide pour l’action standard action2.</span><span class="sxs-lookup"><span data-stu-id="dc646-155">Do not leave the Sequence field empty for standard action Action2.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dc646-156">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="dc646-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dc646-157">Référence ICE du module de fusion</span><span class="sxs-lookup"><span data-stu-id="dc646-157">Merge Module ICE Reference</span></span>](merge-module-ice-reference.md)
</dt> </dl>

 

 



