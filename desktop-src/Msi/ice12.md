---
description: ICE12 valide les tables CustomAction, Directory, AdminExecuteSequence, AdminUISequence, AdvtExecuteSequence, InstallExecuteSequence et InstallUISequence de la base de données Windows Installer.
ms.assetid: c1576aff-ff05-49be-8679-a8bfd01977f5
title: ICE12
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d02756bd357c6e85f60b0c41b72a4a66965fedb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521033"
---
# <a name="ice12"></a><span data-ttu-id="0709d-103">ICE12</span><span class="sxs-lookup"><span data-stu-id="0709d-103">ICE12</span></span>

<span data-ttu-id="0709d-104">ICE12 interroge les tables [CustomAction](customaction-table.md), [Directory](directory-table.md), [AdminExecuteSequence](adminexecutesequence-table.md), [AdminUISequence](adminuisequence-table.md), [AdvtExecuteSequence](advtexecutesequence-table.md), [InstallExecuteSequence](installexecutesequence-table.md)et [InstallUISequence](installuisequence-table.md) pour valider les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="0709d-104">ICE12 queries the [CustomAction](customaction-table.md), [Directory](directory-table.md), [AdminExecuteSequence](adminexecutesequence-table.md), [AdminUISequence](adminuisequence-table.md), [AdvtExecuteSequence](advtexecutesequence-table.md), [InstallExecuteSequence](installexecutesequence-table.md), and [InstallUISequence](installuisequence-table.md) tables to validate the following:</span></span>

-   <span data-ttu-id="0709d-105">Que l' [action CostFinalize](costfinalize-action.md) se produit dans n’importe quelle table de séquences contenant des actions de type [action personnalisée 35](custom-action-type-35.md) ou [type d’action personnalisé 51](custom-action-type-51.md).</span><span class="sxs-lookup"><span data-stu-id="0709d-105">That the [CostFinalize action](costfinalize-action.md) occurs in any sequence table containing actions of the type [Custom Action Type 35](custom-action-type-35.md) or [Custom Action Type 51](custom-action-type-51.md).</span></span>
-   <span data-ttu-id="0709d-106">Que chaque [type d’action personnalisé 35](custom-action-type-35.md) vient après l' [action CostFinalize](costfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="0709d-106">That every [Custom Action Type 35](custom-action-type-35.md) comes after the [CostFinalize action](costfinalize-action.md).</span></span> <span data-ttu-id="0709d-107">dans les tables de séquence.</span><span class="sxs-lookup"><span data-stu-id="0709d-107">in the sequence tables.</span></span>
-   <span data-ttu-id="0709d-108">Chaque [type d’action personnalisé 51](custom-action-type-51.md) qui a une clé étrangère dans la table de répertoires de la colonne source de la table CustomAction vient avant l' [action CostFinalize](costfinalize-action.md) dans les tables de séquence.</span><span class="sxs-lookup"><span data-stu-id="0709d-108">That every [Custom Action Type 51](custom-action-type-51.md) that has a foreign key to the Directory table in the Source column of the CustomAction table comes before the [CostFinalize action](costfinalize-action.md) in the sequence tables.</span></span>

<span data-ttu-id="0709d-109">Notez que ICE12 ne valide pas le texte mis en forme dans la colonne cible de la table CustomAction.</span><span class="sxs-lookup"><span data-stu-id="0709d-109">Note that ICE12 does not validate the formatted text in the Target column of the CustomAction table.</span></span>

## <a name="result"></a><span data-ttu-id="0709d-110">Résultats</span><span class="sxs-lookup"><span data-stu-id="0709d-110">Result</span></span>

<span data-ttu-id="0709d-111">ICE12 publie un message d’erreur si la validation des actions personnalisées qui définissent une propriété de répertoire échoue.</span><span class="sxs-lookup"><span data-stu-id="0709d-111">ICE12 posts an error message if validation of the custom actions that set a directory property fails.</span></span>

## <a name="example"></a><span data-ttu-id="0709d-112">Exemple</span><span class="sxs-lookup"><span data-stu-id="0709d-112">Example</span></span>

<span data-ttu-id="0709d-113">ICE12 publie trois erreurs pour l’exemple indiqué.</span><span class="sxs-lookup"><span data-stu-id="0709d-113">ICE12 would post three errors for the example shown.</span></span>

-   <span data-ttu-id="0709d-114">Pour CA1, le dossier’mondossier’est introuvable dans la table de répertoire</span><span class="sxs-lookup"><span data-stu-id="0709d-114">For CA1, Folder 'MyFolder' not found in Directory table</span></span>
-   <span data-ttu-id="0709d-115">Pour CA2, la séquence « 80 » est antérieure à CostFinalize dans la table InstallExecuteSequence.</span><span class="sxs-lookup"><span data-stu-id="0709d-115">For CA2, Sequence '80' comes before CostFinalize in the InstallExecuteSequence table.</span></span> <span data-ttu-id="0709d-116">Il doit venir après ( CF@100 )</span><span class="sxs-lookup"><span data-stu-id="0709d-116">It must come after (CF@100)</span></span>
-   <span data-ttu-id="0709d-117">Pour CA3, la séquence « 125 » vient après CostFinalize dans la table InstallExecuteSequence.</span><span class="sxs-lookup"><span data-stu-id="0709d-117">For CA3, Sequence '125' comes after CostFinalize in the InstallExecuteSequence table.</span></span> <span data-ttu-id="0709d-118">Il doit précéder ( CF@100 )</span><span class="sxs-lookup"><span data-stu-id="0709d-118">It must come before (CF@100)</span></span>

<span data-ttu-id="0709d-119">[Table CustomAction](customaction-table.md) (partielle)</span><span class="sxs-lookup"><span data-stu-id="0709d-119">[CustomAction Table](customaction-table.md) (partial)</span></span>



| <span data-ttu-id="0709d-120">Action</span><span class="sxs-lookup"><span data-stu-id="0709d-120">Action</span></span> | <span data-ttu-id="0709d-121">Type</span><span class="sxs-lookup"><span data-stu-id="0709d-121">Type</span></span> | <span data-ttu-id="0709d-122">Source</span><span class="sxs-lookup"><span data-stu-id="0709d-122">Source</span></span>        |
|--------|------|---------------|
| <span data-ttu-id="0709d-123">AC1</span><span class="sxs-lookup"><span data-stu-id="0709d-123">CA1</span></span>    | <span data-ttu-id="0709d-124">35</span><span class="sxs-lookup"><span data-stu-id="0709d-124">35</span></span>   | <span data-ttu-id="0709d-125">Mondossier</span><span class="sxs-lookup"><span data-stu-id="0709d-125">MyFolder</span></span>      |
| <span data-ttu-id="0709d-126">CA2</span><span class="sxs-lookup"><span data-stu-id="0709d-126">CA2</span></span>    | <span data-ttu-id="0709d-127">35</span><span class="sxs-lookup"><span data-stu-id="0709d-127">35</span></span>   | <span data-ttu-id="0709d-128">WindowsFolder</span><span class="sxs-lookup"><span data-stu-id="0709d-128">WindowsFolder</span></span> |
| <span data-ttu-id="0709d-129">CA3</span><span class="sxs-lookup"><span data-stu-id="0709d-129">CA3</span></span>    | <span data-ttu-id="0709d-130">51</span><span class="sxs-lookup"><span data-stu-id="0709d-130">51</span></span>   | <span data-ttu-id="0709d-131">WindowsFolder</span><span class="sxs-lookup"><span data-stu-id="0709d-131">WindowsFolder</span></span> |



 

[<span data-ttu-id="0709d-132">Table de répertoire</span><span class="sxs-lookup"><span data-stu-id="0709d-132">Directory Table</span></span>](directory-table.md)



| <span data-ttu-id="0709d-133">Répertoire</span><span class="sxs-lookup"><span data-stu-id="0709d-133">Directory</span></span>     | <span data-ttu-id="0709d-134">Répertoire \_ parent</span><span class="sxs-lookup"><span data-stu-id="0709d-134">Directory\_Parent</span></span> | <span data-ttu-id="0709d-135">DefaultDir</span><span class="sxs-lookup"><span data-stu-id="0709d-135">DefaultDir</span></span>    |
|---------------|-------------------|---------------|
| <span data-ttu-id="0709d-136">TARGETDIR</span><span class="sxs-lookup"><span data-stu-id="0709d-136">TARGETDIR</span></span>     |                   | <span data-ttu-id="0709d-137">SourceDir</span><span class="sxs-lookup"><span data-stu-id="0709d-137">SourceDir</span></span>     |
| <span data-ttu-id="0709d-138">WindowsFolder</span><span class="sxs-lookup"><span data-stu-id="0709d-138">WindowsFolder</span></span> | <span data-ttu-id="0709d-139">TARGETDIR</span><span class="sxs-lookup"><span data-stu-id="0709d-139">TARGETDIR</span></span>         | <span data-ttu-id="0709d-140">WindowsFolder</span><span class="sxs-lookup"><span data-stu-id="0709d-140">WindowsFolder</span></span> |



 

<span data-ttu-id="0709d-141">[Table InstallExecuteSequence](installexecutesequence-table.md) (partielle)</span><span class="sxs-lookup"><span data-stu-id="0709d-141">[InstallExecuteSequence Table](installexecutesequence-table.md) (partial)</span></span>



| <span data-ttu-id="0709d-142">Action</span><span class="sxs-lookup"><span data-stu-id="0709d-142">Action</span></span>       | <span data-ttu-id="0709d-143">Séquence</span><span class="sxs-lookup"><span data-stu-id="0709d-143">Sequence</span></span> |
|--------------|----------|
| <span data-ttu-id="0709d-144">CostFinalize</span><span class="sxs-lookup"><span data-stu-id="0709d-144">CostFinalize</span></span> | <span data-ttu-id="0709d-145">100</span><span class="sxs-lookup"><span data-stu-id="0709d-145">100</span></span>      |
| <span data-ttu-id="0709d-146">CA2</span><span class="sxs-lookup"><span data-stu-id="0709d-146">CA2</span></span>          | <span data-ttu-id="0709d-147">80</span><span class="sxs-lookup"><span data-stu-id="0709d-147">80</span></span>       |
| <span data-ttu-id="0709d-148">CA3</span><span class="sxs-lookup"><span data-stu-id="0709d-148">CA3</span></span>          | <span data-ttu-id="0709d-149">125</span><span class="sxs-lookup"><span data-stu-id="0709d-149">125</span></span>      |



 

<span data-ttu-id="0709d-150">Pour corriger l’erreur pour CA1, remplacez son entrée dans la colonne source de la table CustomAction par une entrée existante dans la table Directory ou ajoutez la valeur mondossier à la table Directory.</span><span class="sxs-lookup"><span data-stu-id="0709d-150">To fix the error for CA1 change its entry in its Source column in the CustomAction table to an existing entry in the Directory table or add MyFolder to the Directory table.</span></span>

<span data-ttu-id="0709d-151">Pour corriger l’erreur pour CA2, modifiez sa séquence dans la table InstallExecuteSequence de sorte qu’elle figure après l’action CostFinalize.</span><span class="sxs-lookup"><span data-stu-id="0709d-151">To fix the error for CA2, change its sequence in the InstallExecuteSequence table such that it comes after the CostFinalize action.</span></span>

<span data-ttu-id="0709d-152">Pour corriger l’erreur pour CA3, modifiez sa séquence dans la table InstallExecuteSequence de sorte qu’elle précède l’action CostFinalize.</span><span class="sxs-lookup"><span data-stu-id="0709d-152">To fix the error for CA3, change its sequence in the InstallExecuteSequence table such that it comes before the CostFinalize action.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0709d-153">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0709d-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0709d-154">Référence ICE</span><span class="sxs-lookup"><span data-stu-id="0709d-154">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



