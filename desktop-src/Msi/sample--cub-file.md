---
description: 'Cet exemple illustre la disposition d’un fichier. CUB contenant deux CIEM. Le programme d’installation exécute les actions personnalisées dans la séquence : ICE01 et ICE08.'
ms.assetid: 609cd16a-4421-4082-855d-229f5ba7117b
title: Exemple de fichier. CUB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e937b779e2a620ffc17cf936e37f74867f3dfdd4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951133"
---
# <a name="sample-cub-file"></a><span data-ttu-id="92707-104">Exemple de fichier. CUB</span><span class="sxs-lookup"><span data-stu-id="92707-104">Sample .cub File</span></span>

<span data-ttu-id="92707-105">Cet exemple illustre la disposition d’un fichier. CUB contenant deux [CIEM](internal-consistency-evaluators-ices.md).</span><span class="sxs-lookup"><span data-stu-id="92707-105">This sample illustrates the layout of a .cub file containing two [ICEs](internal-consistency-evaluators-ices.md).</span></span> <span data-ttu-id="92707-106">Le programme d’installation exécute les actions personnalisées dans la séquence : ICE01 et ICE08.</span><span class="sxs-lookup"><span data-stu-id="92707-106">The installer executes the custom actions in the sequence: ICE01 and ICE08.</span></span>

<span data-ttu-id="92707-107">L’action personnalisée ICE01 est un [type d’action personnalisé 1](custom-action-type-1.md).</span><span class="sxs-lookup"><span data-stu-id="92707-107">The custom action ICE01 is a [Custom Action Type 1](custom-action-type-1.md).</span></span> <span data-ttu-id="92707-108">Il s’agit d’un point d’entrée d’une DLL stockée en tant que flux dans le fichier. CUB.</span><span class="sxs-lookup"><span data-stu-id="92707-108">It is an entry point to a DLL that is stored as a stream in the .cub file.</span></span> <span data-ttu-id="92707-109">Ce flux est listé dans la ice.dll table binaire.</span><span class="sxs-lookup"><span data-stu-id="92707-109">This stream is listed in the Binary Table ice.dll.</span></span>

<span data-ttu-id="92707-110">L’action personnalisée ICE08 est un [type d’action personnalisé 6](custom-action-type-6.md).</span><span class="sxs-lookup"><span data-stu-id="92707-110">The custom action ICE08 is a [Custom Action Type 6](custom-action-type-6.md).</span></span> <span data-ttu-id="92707-111">Il s’agit d’un point d’entrée d’une fonction dans VBScript qui est stockée sous forme de flux dans le fichier. CUB.</span><span class="sxs-lookup"><span data-stu-id="92707-111">It is an entry point to a function in VBScript that is stored as a stream in the .cub file.</span></span> <span data-ttu-id="92707-112">Ce flux est listé dans la table binaire comme ice.vbs.</span><span class="sxs-lookup"><span data-stu-id="92707-112">This stream is listed in the Binary Table as ice.vbs.</span></span>

[<span data-ttu-id="92707-113">Table binaire</span><span class="sxs-lookup"><span data-stu-id="92707-113">Binary Table</span></span>](binary-table.md)



| <span data-ttu-id="92707-114">Nom</span><span class="sxs-lookup"><span data-stu-id="92707-114">Name</span></span>    | <span data-ttu-id="92707-115">Données</span><span class="sxs-lookup"><span data-stu-id="92707-115">Data</span></span>                               |
|---------|------------------------------------|
| <span data-ttu-id="92707-116">ice.vbs</span><span class="sxs-lookup"><span data-stu-id="92707-116">ice.vbs</span></span> | <span data-ttu-id="92707-117">Données binaires non mises en forme de ice.vbs</span><span class="sxs-lookup"><span data-stu-id="92707-117">Unformatted binary data of ice.vbs</span></span> |
| <span data-ttu-id="92707-118">ice.dll</span><span class="sxs-lookup"><span data-stu-id="92707-118">ice.dll</span></span> | <span data-ttu-id="92707-119">Données binaires non mises en forme de ice.dll</span><span class="sxs-lookup"><span data-stu-id="92707-119">Unformatted binary data of ice.dll</span></span> |



 

[<span data-ttu-id="92707-120">Table CustomAction</span><span class="sxs-lookup"><span data-stu-id="92707-120">CustomAction Table</span></span>](customaction-table.md)



| <span data-ttu-id="92707-121">Action</span><span class="sxs-lookup"><span data-stu-id="92707-121">Action</span></span> | <span data-ttu-id="92707-122">Type</span><span class="sxs-lookup"><span data-stu-id="92707-122">Type</span></span> | <span data-ttu-id="92707-123">Source</span><span class="sxs-lookup"><span data-stu-id="92707-123">Source</span></span>  | <span data-ttu-id="92707-124">Cible</span><span class="sxs-lookup"><span data-stu-id="92707-124">Target</span></span> |
|--------|------|---------|--------|
| <span data-ttu-id="92707-125">ICE01</span><span class="sxs-lookup"><span data-stu-id="92707-125">ICE01</span></span>  | <span data-ttu-id="92707-126">1</span><span class="sxs-lookup"><span data-stu-id="92707-126">1</span></span>    | <span data-ttu-id="92707-127">ice.dll</span><span class="sxs-lookup"><span data-stu-id="92707-127">ice.dll</span></span> | <span data-ttu-id="92707-128">ICE01</span><span class="sxs-lookup"><span data-stu-id="92707-128">ICE01</span></span>  |
| <span data-ttu-id="92707-129">ICE08</span><span class="sxs-lookup"><span data-stu-id="92707-129">ICE08</span></span>  | <span data-ttu-id="92707-130">6</span><span class="sxs-lookup"><span data-stu-id="92707-130">6</span></span>    | <span data-ttu-id="92707-131">ice.vbs</span><span class="sxs-lookup"><span data-stu-id="92707-131">ice.vbs</span></span> | <span data-ttu-id="92707-132">ICE02</span><span class="sxs-lookup"><span data-stu-id="92707-132">ICE02</span></span>  |



 

<span data-ttu-id="92707-133">\_Table ICESequence</span><span class="sxs-lookup"><span data-stu-id="92707-133">\_ICESequence Table</span></span>



| <span data-ttu-id="92707-134">Action</span><span class="sxs-lookup"><span data-stu-id="92707-134">Action</span></span> | <span data-ttu-id="92707-135">Condition</span><span class="sxs-lookup"><span data-stu-id="92707-135">Condition</span></span> | <span data-ttu-id="92707-136">Séquence</span><span class="sxs-lookup"><span data-stu-id="92707-136">Sequence</span></span> |
|--------|-----------|----------|
| <span data-ttu-id="92707-137">ICE01</span><span class="sxs-lookup"><span data-stu-id="92707-137">ICE01</span></span>  |           | <span data-ttu-id="92707-138">10</span><span class="sxs-lookup"><span data-stu-id="92707-138">10</span></span>       |
| <span data-ttu-id="92707-139">ICE08</span><span class="sxs-lookup"><span data-stu-id="92707-139">ICE08</span></span>  |           | <span data-ttu-id="92707-140">20</span><span class="sxs-lookup"><span data-stu-id="92707-140">20</span></span>       |



 

<span data-ttu-id="92707-141">\_Table spéciale</span><span class="sxs-lookup"><span data-stu-id="92707-141">\_Special Table</span></span>

<span data-ttu-id="92707-142">ICE01 et ICE08 ne nécessitent pas l’inclusion de tables de traitement spéciales.</span><span class="sxs-lookup"><span data-stu-id="92707-142">ICE01 and ICE08 do not require the inclusion of special processing tables.</span></span> <span data-ttu-id="92707-143">Quand le fichier. CUB contient des tables spéciales, elles doivent également être incluses dans le \_ tableau de validation.</span><span class="sxs-lookup"><span data-stu-id="92707-143">When the .cub file contains special tables they must also be included in the \_Validation Table.</span></span>

[<span data-ttu-id="92707-144">\_Tableau de validation</span><span class="sxs-lookup"><span data-stu-id="92707-144">\_Validation Table</span></span>](-validation-table.md)



| <span data-ttu-id="92707-145">Table de charge de travail</span><span class="sxs-lookup"><span data-stu-id="92707-145">Table</span></span>         | <span data-ttu-id="92707-146">Colonne</span><span class="sxs-lookup"><span data-stu-id="92707-146">Column</span></span>    | <span data-ttu-id="92707-147">Nullable</span><span class="sxs-lookup"><span data-stu-id="92707-147">Nullable</span></span> | <span data-ttu-id="92707-148">MinValue</span><span class="sxs-lookup"><span data-stu-id="92707-148">MinValue</span></span> | <span data-ttu-id="92707-149">MaxValue</span><span class="sxs-lookup"><span data-stu-id="92707-149">MaxValue</span></span> | <span data-ttu-id="92707-150">Keytable</span><span class="sxs-lookup"><span data-stu-id="92707-150">KeyTable</span></span> | <span data-ttu-id="92707-151">KeyColumn</span><span class="sxs-lookup"><span data-stu-id="92707-151">KeyColumn</span></span> | <span data-ttu-id="92707-152">Category</span><span class="sxs-lookup"><span data-stu-id="92707-152">Category</span></span>                         | <span data-ttu-id="92707-153">Définissez</span><span class="sxs-lookup"><span data-stu-id="92707-153">Set</span></span> | <span data-ttu-id="92707-154">Description</span><span class="sxs-lookup"><span data-stu-id="92707-154">Description</span></span> |
|---------------|-----------|----------|----------|----------|----------|-----------|----------------------------------|-----|-------------|
| <span data-ttu-id="92707-155">Binary</span><span class="sxs-lookup"><span data-stu-id="92707-155">Binary</span></span>        | <span data-ttu-id="92707-156">Nom</span><span class="sxs-lookup"><span data-stu-id="92707-156">Name</span></span>      | <span data-ttu-id="92707-157">N</span><span class="sxs-lookup"><span data-stu-id="92707-157">N</span></span>        |          |          |          |           | [<span data-ttu-id="92707-158">Identificateur</span><span class="sxs-lookup"><span data-stu-id="92707-158">Identifier</span></span>](identifier.md)     |     |             |
| <span data-ttu-id="92707-159">Binary</span><span class="sxs-lookup"><span data-stu-id="92707-159">Binary</span></span>        | <span data-ttu-id="92707-160">Données</span><span class="sxs-lookup"><span data-stu-id="92707-160">Data</span></span>      | <span data-ttu-id="92707-161">N</span><span class="sxs-lookup"><span data-stu-id="92707-161">N</span></span>        |          |          |          |           | [<span data-ttu-id="92707-162">Binaire</span><span class="sxs-lookup"><span data-stu-id="92707-162">Binary</span></span>](binary.md)             |     |             |
| <span data-ttu-id="92707-163">CustomAction</span><span class="sxs-lookup"><span data-stu-id="92707-163">CustomAction</span></span>  | <span data-ttu-id="92707-164">Action</span><span class="sxs-lookup"><span data-stu-id="92707-164">Action</span></span>    | <span data-ttu-id="92707-165">N</span><span class="sxs-lookup"><span data-stu-id="92707-165">N</span></span>        |          |          |          |           | [<span data-ttu-id="92707-166">Identificateur</span><span class="sxs-lookup"><span data-stu-id="92707-166">Identifier</span></span>](identifier.md)     |     |             |
| <span data-ttu-id="92707-167">CustomAction</span><span class="sxs-lookup"><span data-stu-id="92707-167">CustomAction</span></span>  | <span data-ttu-id="92707-168">Type</span><span class="sxs-lookup"><span data-stu-id="92707-168">Type</span></span>      | <span data-ttu-id="92707-169">N</span><span class="sxs-lookup"><span data-stu-id="92707-169">N</span></span>        |          |          |          |           | [<span data-ttu-id="92707-170">Integer</span><span class="sxs-lookup"><span data-stu-id="92707-170">Integer</span></span>](integer.md)           |     |             |
| <span data-ttu-id="92707-171">CustomAction</span><span class="sxs-lookup"><span data-stu-id="92707-171">CustomAction</span></span>  | <span data-ttu-id="92707-172">Source</span><span class="sxs-lookup"><span data-stu-id="92707-172">Source</span></span>    | <span data-ttu-id="92707-173">O</span><span class="sxs-lookup"><span data-stu-id="92707-173">Y</span></span>        |          |          |          |           | [<span data-ttu-id="92707-174">CustomSource</span><span class="sxs-lookup"><span data-stu-id="92707-174">CustomSource</span></span>](customsource.md) |     |             |
| <span data-ttu-id="92707-175">CustomAction</span><span class="sxs-lookup"><span data-stu-id="92707-175">CustomAction</span></span>  | <span data-ttu-id="92707-176">Cible</span><span class="sxs-lookup"><span data-stu-id="92707-176">Target</span></span>    | <span data-ttu-id="92707-177">O</span><span class="sxs-lookup"><span data-stu-id="92707-177">Y</span></span>        |          |          |          |           | [<span data-ttu-id="92707-178">Correct</span><span class="sxs-lookup"><span data-stu-id="92707-178">Formatted</span></span>](formatted.md)       |     |             |
| <span data-ttu-id="92707-179">\_ICESequence</span><span class="sxs-lookup"><span data-stu-id="92707-179">\_ICESequence</span></span> | <span data-ttu-id="92707-180">Action</span><span class="sxs-lookup"><span data-stu-id="92707-180">Action</span></span>    | <span data-ttu-id="92707-181">N</span><span class="sxs-lookup"><span data-stu-id="92707-181">N</span></span>        |          |          |          |           | [<span data-ttu-id="92707-182">Identificateur</span><span class="sxs-lookup"><span data-stu-id="92707-182">Identifier</span></span>](identifier.md)     |     |             |
| <span data-ttu-id="92707-183">\_ICESequence</span><span class="sxs-lookup"><span data-stu-id="92707-183">\_ICESequence</span></span> | <span data-ttu-id="92707-184">Condition</span><span class="sxs-lookup"><span data-stu-id="92707-184">Condition</span></span> | <span data-ttu-id="92707-185">O</span><span class="sxs-lookup"><span data-stu-id="92707-185">Y</span></span>        |          |          |          |           | [<span data-ttu-id="92707-186">Condition</span><span class="sxs-lookup"><span data-stu-id="92707-186">Condition</span></span>](condition.md)       |     |             |
| <span data-ttu-id="92707-187">\_ICESequence</span><span class="sxs-lookup"><span data-stu-id="92707-187">\_ICESequence</span></span> | <span data-ttu-id="92707-188">Séquence</span><span class="sxs-lookup"><span data-stu-id="92707-188">Sequence</span></span>  | <span data-ttu-id="92707-189">O</span><span class="sxs-lookup"><span data-stu-id="92707-189">Y</span></span>        |          |          |          |           | [<span data-ttu-id="92707-190">Integer</span><span class="sxs-lookup"><span data-stu-id="92707-190">Integer</span></span>](integer.md)           |     |             |



 

 

 



