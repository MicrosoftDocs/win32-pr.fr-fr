---
description: ICE75 vérifie que toutes les actions personnalisées de type d’action personnalisé 17 (DLL), de type d’action personnalisée 18 (EXE), de type d’action personnalisée 21 (JScript) et de type d’action personnalisée 22 (VBScript) sont séquencées après l’action CostFinalize.
ms.assetid: 831de042-bea6-42da-90a0-3847bb447414
title: ICE75
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23d708552b3ed2d397e29d37abdf0ceed01093fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319918"
---
# <a name="ice75"></a><span data-ttu-id="726f9-103">ICE75</span><span class="sxs-lookup"><span data-stu-id="726f9-103">ICE75</span></span>

<span data-ttu-id="726f9-104">ICE75 vérifie que toutes les actions personnalisées de type d' [action personnalisé 17](custom-action-type-17.md) (dll), de [type d’action personnalisée 18](custom-action-type-18.md) (exe), de [type d’action personnalisée 21](custom-action-type-21.md) (JScript) et de [type d’action personnalisée 22](custom-action-type-22.md) (VBScript) sont séquencées après l' [action CostFinalize](costfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="726f9-104">ICE75 verifies that all [Custom Action Type 17](custom-action-type-17.md) (DLL), [Custom Action Type 18](custom-action-type-18.md) (EXE), [Custom Action type 21](custom-action-type-21.md) (JScript), and [Custom Action Type 22](custom-action-type-22.md) (VBScript) custom actions are sequenced after the [CostFinalize action](costfinalize-action.md).</span></span> <span data-ttu-id="726f9-105">Ces types d’actions personnalisées utilisent un fichier installé comme source.</span><span class="sxs-lookup"><span data-stu-id="726f9-105">These types of custom action use an installed file as their source.</span></span> <span data-ttu-id="726f9-106">ICE75 vérifie la table [InstallUISequence](installuisequence-table.md), la table [InstallExecuteSequence](installexecutesequence-table.md), la table [AdminUISequence](adminuisequence-table.md)et la [table AdminExecuteSequence](adminexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="726f9-106">ICE75 checks the [InstallUISequence Table](installuisequence-table.md), [InstallExecuteSequence Table](installexecutesequence-table.md), [AdminUISequence Table](adminuisequence-table.md), and [AdminExecuteSequence Table](adminexecutesequence-table.md).</span></span> <span data-ttu-id="726f9-107">Notez que l’action CostFinalize est requise dans ces tables de séquence.</span><span class="sxs-lookup"><span data-stu-id="726f9-107">Note that the CostFinalize action is required in these sequence tables.</span></span>

## <a name="result"></a><span data-ttu-id="726f9-108">Résultats</span><span class="sxs-lookup"><span data-stu-id="726f9-108">Result</span></span>

<span data-ttu-id="726f9-109">ICE75 publie une erreur s’il trouve une action personnalisée à l’aide d’un fichier installé comme fichier source qui n’est pas séquencé après l’action CostFinalize.</span><span class="sxs-lookup"><span data-stu-id="726f9-109">ICE75 posts an error if it finds a custom action using an installed file as a source file that is not sequenced after the CostFinalize action.</span></span>

## <a name="example"></a><span data-ttu-id="726f9-110">Exemple</span><span class="sxs-lookup"><span data-stu-id="726f9-110">Example</span></span>

<span data-ttu-id="726f9-111">ICE75 signale les erreurs suivantes pour l’exemple illustré :</span><span class="sxs-lookup"><span data-stu-id="726f9-111">ICE75 reports the following errors for the example shown:</span></span>

``` syntax
CostFinalize is missing from 'AdminUISequence'. CA_FileExe is a custom
 action whose source is an installed file. It must be sequenced after 
the CostFinalize action.
 
CA_FileDLL is a custom action whose source is an installed file.  It 
must be sequenced after the CostFinalize action in the 
AdminExecuteSequence table
```

<span data-ttu-id="726f9-112">[Table CustomAction](customaction-table.md) (partielle)</span><span class="sxs-lookup"><span data-stu-id="726f9-112">[CustomAction Table](customaction-table.md) (partial)</span></span>



| <span data-ttu-id="726f9-113">Action</span><span class="sxs-lookup"><span data-stu-id="726f9-113">Action</span></span>      | <span data-ttu-id="726f9-114">Type</span><span class="sxs-lookup"><span data-stu-id="726f9-114">Type</span></span> | <span data-ttu-id="726f9-115">Source</span><span class="sxs-lookup"><span data-stu-id="726f9-115">Source</span></span>  |
|-------------|------|---------|
| <span data-ttu-id="726f9-116">\_FILEEXE ca</span><span class="sxs-lookup"><span data-stu-id="726f9-116">CA\_FileExe</span></span> | <span data-ttu-id="726f9-117">18</span><span class="sxs-lookup"><span data-stu-id="726f9-117">18</span></span>   | <span data-ttu-id="726f9-118">FileExe</span><span class="sxs-lookup"><span data-stu-id="726f9-118">FileExe</span></span> |
| <span data-ttu-id="726f9-119">\_FILEDLL ca</span><span class="sxs-lookup"><span data-stu-id="726f9-119">CA\_FileDLL</span></span> | <span data-ttu-id="726f9-120">17</span><span class="sxs-lookup"><span data-stu-id="726f9-120">17</span></span>   | <span data-ttu-id="726f9-121">FileDLL</span><span class="sxs-lookup"><span data-stu-id="726f9-121">FileDLL</span></span> |



 

<span data-ttu-id="726f9-122">[Table AdminUISequence](adminuisequence-table.md) (partielle)</span><span class="sxs-lookup"><span data-stu-id="726f9-122">[AdminUISequence Table](adminuisequence-table.md) (partial)</span></span>



| <span data-ttu-id="726f9-123">Action</span><span class="sxs-lookup"><span data-stu-id="726f9-123">Action</span></span>      | <span data-ttu-id="726f9-124">Séquence</span><span class="sxs-lookup"><span data-stu-id="726f9-124">Sequence</span></span> |
|-------------|----------|
| <span data-ttu-id="726f9-125">\_FILEEXE ca</span><span class="sxs-lookup"><span data-stu-id="726f9-125">CA\_FileExe</span></span> | <span data-ttu-id="726f9-126">1100</span><span class="sxs-lookup"><span data-stu-id="726f9-126">1100</span></span>     |



 

<span data-ttu-id="726f9-127">[Table AdminExecuteSequence](adminexecutesequence-table.md) (partielle)</span><span class="sxs-lookup"><span data-stu-id="726f9-127">[AdminExecuteSequence Table](adminexecutesequence-table.md) (partial)</span></span>



| <span data-ttu-id="726f9-128">Action</span><span class="sxs-lookup"><span data-stu-id="726f9-128">Action</span></span>       | <span data-ttu-id="726f9-129">Séquence</span><span class="sxs-lookup"><span data-stu-id="726f9-129">Sequence</span></span> |
|--------------|----------|
| <span data-ttu-id="726f9-130">\_FILEDLL ca</span><span class="sxs-lookup"><span data-stu-id="726f9-130">CA\_FileDLL</span></span>  | <span data-ttu-id="726f9-131">800</span><span class="sxs-lookup"><span data-stu-id="726f9-131">800</span></span>      |
| <span data-ttu-id="726f9-132">CostFinalize</span><span class="sxs-lookup"><span data-stu-id="726f9-132">CostFinalize</span></span> | <span data-ttu-id="726f9-133">1 000</span><span class="sxs-lookup"><span data-stu-id="726f9-133">1000</span></span>     |



 

<span data-ttu-id="726f9-134">Pour corriger les erreurs, séquencez les actions personnalisées après l’action CostFinalize.</span><span class="sxs-lookup"><span data-stu-id="726f9-134">To fix the errors, sequence the custom actions after the CostFinalize action.</span></span>

## <a name="related-topics"></a><span data-ttu-id="726f9-135">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="726f9-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="726f9-136">Référence ICE</span><span class="sxs-lookup"><span data-stu-id="726f9-136">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



