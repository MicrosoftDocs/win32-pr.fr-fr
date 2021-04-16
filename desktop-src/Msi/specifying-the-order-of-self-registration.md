---
description: Notez que vous ne pouvez pas spécifier l’ordre dans lequel le programme d’installation enregistre ou annule l’enregistrement automatique des dll à l’aide des actions SelfRegModules et SelfUnRegModules.
ms.assetid: 46ee5ea2-35fd-4352-8a45-572d6fb5e080
title: Spécification de l’ordre d’inscription automatique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d99587f6e6bdd8726f2cdc584fc2f399d81ae91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104485377"
---
# <a name="specifying-the-order-of-self-registration"></a><span data-ttu-id="b4d6a-103">Spécification de l’ordre d’inscription automatique</span><span class="sxs-lookup"><span data-stu-id="b4d6a-103">Specifying the Order of Self Registration</span></span>

<span data-ttu-id="b4d6a-104">Notez que vous ne pouvez pas spécifier l’ordre dans lequel le programme d’installation enregistre ou annule l’enregistrement automatique des dll à l’aide des actions [SelfRegModules](selfregmodules-action.md) et [SelfUnRegModules](selfunregmodules-action.md) .</span><span class="sxs-lookup"><span data-stu-id="b4d6a-104">Note that you cannot specify the order in which the installer registers or unregisters self-registering DLLs by using the [SelfRegModules](selfregmodules-action.md) and [SelfUnRegModules](selfunregmodules-action.md) actions.</span></span> <span data-ttu-id="b4d6a-105">Ces actions inscrivent tous les modules listés dans la [table Selfreg](selfreg-table.md).</span><span class="sxs-lookup"><span data-stu-id="b4d6a-105">These actions register all the modules listed in the [SelfReg table](selfreg-table.md).</span></span> <span data-ttu-id="b4d6a-106">Le programme d’installation n’enregistre pas automatiquement les fichiers. exe.</span><span class="sxs-lookup"><span data-stu-id="b4d6a-106">The installer does not self-register .exe files.</span></span>

<span data-ttu-id="b4d6a-107">Pour spécifier l’ordre dans lequel le programme d’installation inscrit ou désinscrit des modules, vous devez utiliser deux [actions personnalisées](custom-actions.md) pour chaque module.</span><span class="sxs-lookup"><span data-stu-id="b4d6a-107">To specify the order in which the installer registers or unregisters modules, you must use two [custom actions](custom-actions.md) for each module.</span></span> <span data-ttu-id="b4d6a-108">Une action personnalisée pour DllRegisterServer et une seconde pour DllUnregisterServer.</span><span class="sxs-lookup"><span data-stu-id="b4d6a-108">One custom action for DllRegisterServer and a second for DllUnregisterServer.</span></span> <span data-ttu-id="b4d6a-109">Ces actions personnalisées doivent ensuite être créées dans la [table InstallExecuteSequence](installexecutesequence-table.md) au point de l’ordre où la dll doit être inscrite ou désinscrite.</span><span class="sxs-lookup"><span data-stu-id="b4d6a-109">These custom actions must then be authored in the [InstallExecuteSequence table](installexecutesequence-table.md) at the point in the sequence wherever the DLL is to be registered or unregistered.</span></span>

<span data-ttu-id="b4d6a-110">L’exemple suivant montre comment créer la base de données pour planifier l’inscription automatique d’une DLL à un point particulier dans la séquence d’action.</span><span class="sxs-lookup"><span data-stu-id="b4d6a-110">The following example illustrates how to author the database to schedule the self-registration of a DLL at a particular point in the action sequence.</span></span>

<span data-ttu-id="b4d6a-111">[Table de fichiers](file-table.md) (partielle)</span><span class="sxs-lookup"><span data-stu-id="b4d6a-111">[File Table](file-table.md) (partial)</span></span>



| <span data-ttu-id="b4d6a-112">Fichier</span><span class="sxs-lookup"><span data-stu-id="b4d6a-112">File</span></span>  | <span data-ttu-id="b4d6a-113">-\_</span><span class="sxs-lookup"><span data-stu-id="b4d6a-113">Component\_</span></span> | <span data-ttu-id="b4d6a-114">FileName</span><span class="sxs-lookup"><span data-stu-id="b4d6a-114">FileName</span></span>  | <span data-ttu-id="b4d6a-115">Séquence</span><span class="sxs-lookup"><span data-stu-id="b4d6a-115">Sequence</span></span> |
|-------|-------------|-----------|----------|
| <span data-ttu-id="b4d6a-116">mydll</span><span class="sxs-lookup"><span data-stu-id="b4d6a-116">mydll</span></span> | <span data-ttu-id="b4d6a-117">myComponent</span><span class="sxs-lookup"><span data-stu-id="b4d6a-117">myComponent</span></span> | <span data-ttu-id="b4d6a-118">Mydll.dll</span><span class="sxs-lookup"><span data-stu-id="b4d6a-118">Mydll.dll</span></span> | <span data-ttu-id="b4d6a-119">13</span><span class="sxs-lookup"><span data-stu-id="b4d6a-119">13</span></span>       |



 

<span data-ttu-id="b4d6a-120">[Table des composants](component-table.md) (partielle)</span><span class="sxs-lookup"><span data-stu-id="b4d6a-120">[Component Table](component-table.md) (partial)</span></span>



| <span data-ttu-id="b4d6a-121">Composant</span><span class="sxs-lookup"><span data-stu-id="b4d6a-121">Component</span></span>   | <span data-ttu-id="b4d6a-122">ComponentId</span><span class="sxs-lookup"><span data-stu-id="b4d6a-122">ComponentId</span></span> | <span data-ttu-id="b4d6a-123">Répertoire\_</span><span class="sxs-lookup"><span data-stu-id="b4d6a-123">Directory\_</span></span> | <span data-ttu-id="b4d6a-124">KeyPath</span><span class="sxs-lookup"><span data-stu-id="b4d6a-124">KeyPath</span></span> |
|-------------|-------------|-------------|---------|
| <span data-ttu-id="b4d6a-125">myComponent</span><span class="sxs-lookup"><span data-stu-id="b4d6a-125">myComponent</span></span> | <span data-ttu-id="b4d6a-126">{*GUID*}</span><span class="sxs-lookup"><span data-stu-id="b4d6a-126">{*a GUID*}</span></span>  | <span data-ttu-id="b4d6a-127">mondossier</span><span class="sxs-lookup"><span data-stu-id="b4d6a-127">myFolder</span></span>    | <span data-ttu-id="b4d6a-128">mydll</span><span class="sxs-lookup"><span data-stu-id="b4d6a-128">mydll</span></span>   |



 

[<span data-ttu-id="b4d6a-129">Table de répertoire</span><span class="sxs-lookup"><span data-stu-id="b4d6a-129">Directory Table</span></span>](directory-table.md)



| <span data-ttu-id="b4d6a-130">Répertoire</span><span class="sxs-lookup"><span data-stu-id="b4d6a-130">Directory</span></span> | <span data-ttu-id="b4d6a-131">Répertoire \_ parent</span><span class="sxs-lookup"><span data-stu-id="b4d6a-131">Directory\_Parent</span></span> | <span data-ttu-id="b4d6a-132">DefaultDir</span><span class="sxs-lookup"><span data-stu-id="b4d6a-132">DefaultDir</span></span>          |
|-----------|-------------------|---------------------|
| <span data-ttu-id="b4d6a-133">TARGETDIR</span><span class="sxs-lookup"><span data-stu-id="b4d6a-133">TARGETDIR</span></span> |                   | <span data-ttu-id="b4d6a-134">SourceDir</span><span class="sxs-lookup"><span data-stu-id="b4d6a-134">SourceDir</span></span>           |
| <span data-ttu-id="b4d6a-135">mondossier</span><span class="sxs-lookup"><span data-stu-id="b4d6a-135">myFolder</span></span>  | <span data-ttu-id="b4d6a-136">TARGETDIR</span><span class="sxs-lookup"><span data-stu-id="b4d6a-136">TARGETDIR</span></span>         | <span data-ttu-id="b4d6a-137">mondossier \| mon dossier</span><span class="sxs-lookup"><span data-stu-id="b4d6a-137">myFolder\|My Folder</span></span> |



 

[<span data-ttu-id="b4d6a-138">Table CustomAction</span><span class="sxs-lookup"><span data-stu-id="b4d6a-138">CustomAction Table</span></span>](customaction-table.md)



| <span data-ttu-id="b4d6a-139">Action</span><span class="sxs-lookup"><span data-stu-id="b4d6a-139">Action</span></span>     | <span data-ttu-id="b4d6a-140">Type</span><span class="sxs-lookup"><span data-stu-id="b4d6a-140">Type</span></span> | <span data-ttu-id="b4d6a-141">Source</span><span class="sxs-lookup"><span data-stu-id="b4d6a-141">Source</span></span>   | <span data-ttu-id="b4d6a-142">Cible</span><span class="sxs-lookup"><span data-stu-id="b4d6a-142">Target</span></span>                                     |
|------------|------|----------|--------------------------------------------|
| <span data-ttu-id="b4d6a-143">mydllREG</span><span class="sxs-lookup"><span data-stu-id="b4d6a-143">mydllREG</span></span>   | <span data-ttu-id="b4d6a-144">3170</span><span class="sxs-lookup"><span data-stu-id="b4d6a-144">3170</span></span> | <span data-ttu-id="b4d6a-145">mondossier</span><span class="sxs-lookup"><span data-stu-id="b4d6a-145">myFolder</span></span> | <span data-ttu-id="b4d6a-146">« \[ SystemFolder \] msiexec »/y « \[ \# mydll \] »</span><span class="sxs-lookup"><span data-stu-id="b4d6a-146">"\[SystemFolder\]msiexec" /y "\[\#mydll\]"</span></span> |
| <span data-ttu-id="b4d6a-147">mydllUNREG</span><span class="sxs-lookup"><span data-stu-id="b4d6a-147">mydllUNREG</span></span> | <span data-ttu-id="b4d6a-148">3170</span><span class="sxs-lookup"><span data-stu-id="b4d6a-148">3170</span></span> | <span data-ttu-id="b4d6a-149">mondossier</span><span class="sxs-lookup"><span data-stu-id="b4d6a-149">myFolder</span></span> | <span data-ttu-id="b4d6a-150">« \[ SystemFolder \] msiexec "/z" \[ \# mydll \] "</span><span class="sxs-lookup"><span data-stu-id="b4d6a-150">"\[SystemFolder\]msiexec" /z "\[\#mydll\]"</span></span> |



 

<span data-ttu-id="b4d6a-151">[Table InstallExecuteSequence](installexecutesequence-table.md) (partielle)</span><span class="sxs-lookup"><span data-stu-id="b4d6a-151">[InstallExecuteSequence Table](installexecutesequence-table.md) (partial)</span></span>



| <span data-ttu-id="b4d6a-152">Action</span><span class="sxs-lookup"><span data-stu-id="b4d6a-152">Action</span></span>           | <span data-ttu-id="b4d6a-153">Condition</span><span class="sxs-lookup"><span data-stu-id="b4d6a-153">Condition</span></span>         | <span data-ttu-id="b4d6a-154">Séquence</span><span class="sxs-lookup"><span data-stu-id="b4d6a-154">Sequence</span></span> |
|------------------|-------------------|----------|
| <span data-ttu-id="b4d6a-155">SelfUnregModules</span><span class="sxs-lookup"><span data-stu-id="b4d6a-155">SelfUnregModules</span></span> |                   | <span data-ttu-id="b4d6a-156">2 200</span><span class="sxs-lookup"><span data-stu-id="b4d6a-156">2200</span></span>     |
| <span data-ttu-id="b4d6a-157">mydllUNREG</span><span class="sxs-lookup"><span data-stu-id="b4d6a-157">mydllUNREG</span></span>       | <span data-ttu-id="b4d6a-158">$myComponent = 2</span><span class="sxs-lookup"><span data-stu-id="b4d6a-158">$myComponent=2</span></span>    | <span data-ttu-id="b4d6a-159">2201</span><span class="sxs-lookup"><span data-stu-id="b4d6a-159">2201</span></span>     |
| <span data-ttu-id="b4d6a-160">RemoveFiles</span><span class="sxs-lookup"><span data-stu-id="b4d6a-160">RemoveFiles</span></span>      |                   | <span data-ttu-id="b4d6a-161">3 500</span><span class="sxs-lookup"><span data-stu-id="b4d6a-161">3500</span></span>     |
| <span data-ttu-id="b4d6a-162">InstallFiles</span><span class="sxs-lookup"><span data-stu-id="b4d6a-162">InstallFiles</span></span>     |                   | <span data-ttu-id="b4d6a-163">4000</span><span class="sxs-lookup"><span data-stu-id="b4d6a-163">4000</span></span>     |
| <span data-ttu-id="b4d6a-164">SelfRegModules</span><span class="sxs-lookup"><span data-stu-id="b4d6a-164">SelfRegModules</span></span>   |                   | <span data-ttu-id="b4d6a-165">6500</span><span class="sxs-lookup"><span data-stu-id="b4d6a-165">6500</span></span>     |
| <span data-ttu-id="b4d6a-166">mydllREG</span><span class="sxs-lookup"><span data-stu-id="b4d6a-166">mydllREG</span></span>         | <span data-ttu-id="b4d6a-167">$myComponent>2</span><span class="sxs-lookup"><span data-stu-id="b4d6a-167">$myComponent>2</span></span> | <span data-ttu-id="b4d6a-168">6501</span><span class="sxs-lookup"><span data-stu-id="b4d6a-168">6501</span></span>     |



 

 

 



