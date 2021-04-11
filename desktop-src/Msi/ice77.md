---
description: ICE77 vérifie que les actions personnalisées avec le jeu de bits msidbCustomActionTypeInScript sont séquencées après l’action InstallInitialize et avant l’action InstallFinalize.
ms.assetid: 291cf731-b7e6-44c2-a8ec-78e0e037d1f5
title: ICE77
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15e072692b76cfd63bf62c5fd23f612a445e5fd7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113855"
---
# <a name="ice77"></a><span data-ttu-id="ae74b-103">ICE77</span><span class="sxs-lookup"><span data-stu-id="ae74b-103">ICE77</span></span>

<span data-ttu-id="ae74b-104">ICE77 vérifie que les actions personnalisées avec le jeu de bits **msidbCustomActionTypeInScript** sont séquencées après l' [action InstallInitialize](installinitialize-action.md) et avant l' [action InstallFinalize](installfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="ae74b-104">ICE77 verifies that custom actions with the **msidbCustomActionTypeInScript** bit set are sequenced after the [InstallInitialize action](installinitialize-action.md) and before the [InstallFinalize action](installfinalize-action.md).</span></span> <span data-ttu-id="ae74b-105">ICE77 vérifie la séquence dans la [table InstallExecuteSequence](installexecutesequence-table.md) et la [table AdminExecuteSequence](adminexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="ae74b-105">ICE77 checks the sequence in the [InstallExecuteSequence table](installexecutesequence-table.md) and [AdminExecuteSequence table](adminexecutesequence-table.md).</span></span>

## <a name="result"></a><span data-ttu-id="ae74b-106">Résultats</span><span class="sxs-lookup"><span data-stu-id="ae74b-106">Result</span></span>

<span data-ttu-id="ae74b-107">ICE77 publie une erreur si une action personnalisée dans le script est séquencée avant l’action InstallInitialize ou après l’action InstallFinalize.</span><span class="sxs-lookup"><span data-stu-id="ae74b-107">ICE77 posts an error if an in-script custom action is sequenced before the InstallInitialize action or after the InstallFinalize action.</span></span>

<span data-ttu-id="ae74b-108">ICE77 publie une erreur si l’action InstallInitialize ou l’action InstallFinalize est manquante.</span><span class="sxs-lookup"><span data-stu-id="ae74b-108">ICE77 posts an error if the InstallInitialize action or the InstallFinalize action is missing.</span></span>

## <a name="example"></a><span data-ttu-id="ae74b-109">Exemple</span><span class="sxs-lookup"><span data-stu-id="ae74b-109">Example</span></span>

<span data-ttu-id="ae74b-110">ICE77 signale les erreurs suivantes pour l’exemple :</span><span class="sxs-lookup"><span data-stu-id="ae74b-110">ICE77 reports the following errors for the example:</span></span>

``` syntax
InstallFinalize is missing from 'InstallExecuteSequence'. 
CA_InScriptInstall is a in-script custom action. It must be sequenced 
before the InstallFinalize action.
 
CA_InScriptAdmin is a in-script custom action.  It must be sequenced 
in between the InstallInitialize action and the InstallFinalize action 
in the AdminExecuteSequence Sequence table.
```

<span data-ttu-id="ae74b-111">[Table CustomAction](customaction-table.md) (partielle)</span><span class="sxs-lookup"><span data-stu-id="ae74b-111">[CustomAction Table](customaction-table.md) (partial)</span></span>



| <span data-ttu-id="ae74b-112">Action</span><span class="sxs-lookup"><span data-stu-id="ae74b-112">Action</span></span>              | <span data-ttu-id="ae74b-113">Type</span><span class="sxs-lookup"><span data-stu-id="ae74b-113">Type</span></span> |
|---------------------|------|
| <span data-ttu-id="ae74b-114">\_INSCRIPTINSTALL ca</span><span class="sxs-lookup"><span data-stu-id="ae74b-114">CA\_InScriptInstall</span></span> | <span data-ttu-id="ae74b-115">1025</span><span class="sxs-lookup"><span data-stu-id="ae74b-115">1025</span></span> |
| <span data-ttu-id="ae74b-116">\_INSCRIPTADMIN ca</span><span class="sxs-lookup"><span data-stu-id="ae74b-116">CA\_InScriptAdmin</span></span>   | <span data-ttu-id="ae74b-117">1026</span><span class="sxs-lookup"><span data-stu-id="ae74b-117">1026</span></span> |



 

<span data-ttu-id="ae74b-118">[Table InstallExecuteSequence](installexecutesequence-table.md) (partielle)</span><span class="sxs-lookup"><span data-stu-id="ae74b-118">[InstallExecuteSequence Table](installexecutesequence-table.md) (partial)</span></span>



| <span data-ttu-id="ae74b-119">Action</span><span class="sxs-lookup"><span data-stu-id="ae74b-119">Action</span></span>              | <span data-ttu-id="ae74b-120">Séquence</span><span class="sxs-lookup"><span data-stu-id="ae74b-120">Sequence</span></span> |
|---------------------|----------|
| <span data-ttu-id="ae74b-121">\_INSCRIPTINSTALL ca</span><span class="sxs-lookup"><span data-stu-id="ae74b-121">CA\_InScriptInstall</span></span> | <span data-ttu-id="ae74b-122">2000</span><span class="sxs-lookup"><span data-stu-id="ae74b-122">2000</span></span>     |
| <span data-ttu-id="ae74b-123">InstallInitialize</span><span class="sxs-lookup"><span data-stu-id="ae74b-123">InstallInitialize</span></span>   | <span data-ttu-id="ae74b-124">1500</span><span class="sxs-lookup"><span data-stu-id="ae74b-124">1500</span></span>     |



 

<span data-ttu-id="ae74b-125">[Table AdminExecuteSequence](adminexecutesequence-table.md) (partielle)</span><span class="sxs-lookup"><span data-stu-id="ae74b-125">[AdminExecuteSequence Table](adminexecutesequence-table.md) (partial)</span></span>



| <span data-ttu-id="ae74b-126">Action</span><span class="sxs-lookup"><span data-stu-id="ae74b-126">Action</span></span>            | <span data-ttu-id="ae74b-127">Séquence</span><span class="sxs-lookup"><span data-stu-id="ae74b-127">Sequence</span></span> |
|-------------------|----------|
| <span data-ttu-id="ae74b-128">\_INSCRIPTADMIN ca</span><span class="sxs-lookup"><span data-stu-id="ae74b-128">CA\_InScriptAdmin</span></span> | <span data-ttu-id="ae74b-129">1400</span><span class="sxs-lookup"><span data-stu-id="ae74b-129">1400</span></span>     |
| <span data-ttu-id="ae74b-130">InstallInitialize</span><span class="sxs-lookup"><span data-stu-id="ae74b-130">InstallInitialize</span></span> | <span data-ttu-id="ae74b-131">1500</span><span class="sxs-lookup"><span data-stu-id="ae74b-131">1500</span></span>     |
| <span data-ttu-id="ae74b-132">InstallFinalize</span><span class="sxs-lookup"><span data-stu-id="ae74b-132">InstallFinalize</span></span>   | <span data-ttu-id="ae74b-133">6600</span><span class="sxs-lookup"><span data-stu-id="ae74b-133">6600</span></span>     |



 

<span data-ttu-id="ae74b-134">Pour corriger les erreurs, séquencez les actions personnalisées dans le script après l’action InstallInitialize et avant l’action InstallFinalize.</span><span class="sxs-lookup"><span data-stu-id="ae74b-134">To fix the errors, sequence the in-script custom actions after the InstallInitialize action and before the InstallFinalize action.</span></span> <span data-ttu-id="ae74b-135">Les actions InstallInitialize et InstallFinalize doivent être présentes dans la table InstallExecuteSequence et la table AdminExecuteSequence.</span><span class="sxs-lookup"><span data-stu-id="ae74b-135">The InstallInitialize and InstallFinalize actions must be present in the InstallExecuteSequence table and the AdminExecuteSequence table.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ae74b-136">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ae74b-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ae74b-137">Référence ICE</span><span class="sxs-lookup"><span data-stu-id="ae74b-137">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



