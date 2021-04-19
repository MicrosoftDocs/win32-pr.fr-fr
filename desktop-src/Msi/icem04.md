---
description: ICEM04 vérifie que les tables vides requises du module de fusion sont vides. Si vous ne corrigez pas une erreur signalant que les rapports ICEM04 peuvent entraîner une fusion incorrecte du module de fusion.
ms.assetid: c6f64f5e-be65-485b-8831-e377535bd335
title: ICEM04
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2ef993690ae690e0651db1538196998c4dd28c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518980"
---
# <a name="icem04"></a><span data-ttu-id="2a42e-104">ICEM04</span><span class="sxs-lookup"><span data-stu-id="2a42e-104">ICEM04</span></span>

<span data-ttu-id="2a42e-105">ICEM04 vérifie que les tables vides requises du module de fusion sont vides.</span><span class="sxs-lookup"><span data-stu-id="2a42e-105">ICEM04 verifies that the merge module's required empty tables are empty.</span></span> <span data-ttu-id="2a42e-106">Si vous ne corrigez pas une erreur signalant que les rapports ICEM04 peuvent entraîner une fusion incorrecte du module de fusion.</span><span class="sxs-lookup"><span data-stu-id="2a42e-106">Failure to fix an error that ICEM04 reports can result in incorrect merging of the merge module.</span></span>

## <a name="result"></a><span data-ttu-id="2a42e-107">Résultats</span><span class="sxs-lookup"><span data-stu-id="2a42e-107">Result</span></span>

<span data-ttu-id="2a42e-108">ICEM04 publie une erreur lorsque les tables vides requises du module de fusion ne sont pas vides.</span><span class="sxs-lookup"><span data-stu-id="2a42e-108">ICEM04 posts an error when the merge module's required empty tables are not empty.</span></span>

## <a name="example"></a><span data-ttu-id="2a42e-109">Exemple</span><span class="sxs-lookup"><span data-stu-id="2a42e-109">Example</span></span>

<span data-ttu-id="2a42e-110">ICEM04 publie les messages d’erreur suivants pour un module qui contient les entrées de base de données affichées.</span><span class="sxs-lookup"><span data-stu-id="2a42e-110">ICEM04 posts the following error messages for a module that contains the database entries shown.</span></span>

``` syntax
An empty FeatureComponents table is required in a Merge Module.

The Merge Module contains the 'ModuleInstallExecuteSequence' table. It 
must therefore have an empty 'InstallExecuteSequence' table.

Action 'CostInitialize' found in the AdvtExecuteSequence table. This 
table must be empty in a Merge Module
```

<span data-ttu-id="2a42e-111">Le tableau suivant présente une [table AdvtExecuteSequence](advtexecutesequence-table.md)partielle.</span><span class="sxs-lookup"><span data-stu-id="2a42e-111">The following table shows you a partial [AdvtExecuteSequence Table](advtexecutesequence-table.md).</span></span>



| <span data-ttu-id="2a42e-112">Action</span><span class="sxs-lookup"><span data-stu-id="2a42e-112">Action</span></span>         | <span data-ttu-id="2a42e-113">Séquence</span><span class="sxs-lookup"><span data-stu-id="2a42e-113">Sequence</span></span> |
|----------------|----------|
| <span data-ttu-id="2a42e-114">CostInitialize</span><span class="sxs-lookup"><span data-stu-id="2a42e-114">CostInitialize</span></span> | <span data-ttu-id="2a42e-115">1</span><span class="sxs-lookup"><span data-stu-id="2a42e-115">1</span></span>        |



 

<span data-ttu-id="2a42e-116">La liste suivante affiche le contenu partiel de MergeModule :</span><span class="sxs-lookup"><span data-stu-id="2a42e-116">The following list shows you the partial contents of MergeModule:</span></span>

-   <span data-ttu-id="2a42e-117">ModuleInstallExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="2a42e-117">ModuleInstallExecuteSequence</span></span>
-   <span data-ttu-id="2a42e-118">ModuleAdvtExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="2a42e-118">ModuleAdvtExecuteSequence</span></span>
-   <span data-ttu-id="2a42e-119">InstallUISequence</span><span class="sxs-lookup"><span data-stu-id="2a42e-119">InstallUISequence</span></span>

<span data-ttu-id="2a42e-120">L’exemple suivant montre une autre erreur possible.</span><span class="sxs-lookup"><span data-stu-id="2a42e-120">The following example shows you another possible error.</span></span>

``` syntax
Feature-Component '[1].[2]' found in the FeatureComponents table. The 
FeatureComponents table must be empty in a Merge Module.
```

<span data-ttu-id="2a42e-121">Si un module de fusion contient une table de séquence de module, il doit contenir la table de séquences vide correspondante, que la table de séquence de module soit vide ou non.</span><span class="sxs-lookup"><span data-stu-id="2a42e-121">If a merge module contains a module sequence table, it must contain the corresponding empty sequence table, whether or not the module sequence table is empty.</span></span> <span data-ttu-id="2a42e-122">Par exemple, si le module de fusion contient la [table ModuleAdminExecuteSequence](moduleadminexecutesequence-table.md), il doit également contenir une table AdminExecuteSequence vide.</span><span class="sxs-lookup"><span data-stu-id="2a42e-122">For example, if the merge module contains the [ModuleAdminExecuteSequence Table](moduleadminexecutesequence-table.md), it must also contain an empty AdminExecuteSequence table.</span></span>

<span data-ttu-id="2a42e-123">La [table FeatureComponents](featurecomponents-table.md) est requise dans tous les modules de fusion et doit être vide.</span><span class="sxs-lookup"><span data-stu-id="2a42e-123">The [FeatureComponents Table](featurecomponents-table.md) is required in all merge modules and must be empty.</span></span>

<span data-ttu-id="2a42e-124">La procédure suivante vous montre comment corriger les erreurs.</span><span class="sxs-lookup"><span data-stu-id="2a42e-124">The following procedure shows you how to fix errors.</span></span>

<span data-ttu-id="2a42e-125">**Pour résoudre les erreurs**</span><span class="sxs-lookup"><span data-stu-id="2a42e-125">**To fix errors**</span></span>

1.  <span data-ttu-id="2a42e-126">Ajoutez une [table FeatureComponents](featurecomponents-table.md) vide au module de fusion.</span><span class="sxs-lookup"><span data-stu-id="2a42e-126">Add an empty [FeatureComponents Table](featurecomponents-table.md) to the merge module.</span></span>
2.  <span data-ttu-id="2a42e-127">Ajoutez une [table InstallExecuteSequence](installexecutesequence-table.md) vide au module de fusion.</span><span class="sxs-lookup"><span data-stu-id="2a42e-127">Add an empty [InstallExecuteSequence Table](installexecutesequence-table.md) to the merge module.</span></span>
3.  <span data-ttu-id="2a42e-128">Supprimez l’action « CostInitialize » de la [table AdvtExecuteSequence](advtexecutesequence-table.md).</span><span class="sxs-lookup"><span data-stu-id="2a42e-128">Remove the 'CostInitialize' action from the [AdvtExecuteSequence Table](advtexecutesequence-table.md).</span></span>
    > [!Note]  
    > <span data-ttu-id="2a42e-129">Cette table doit être vide dans un module de fusion.</span><span class="sxs-lookup"><span data-stu-id="2a42e-129">This table must be empty in a merge module.</span></span> <span data-ttu-id="2a42e-130">Les actions doivent apparaître uniquement dans la table ModuleAdvtExecuteSequence.</span><span class="sxs-lookup"><span data-stu-id="2a42e-130">Actions should only appear in the ModuleAdvtExecuteSequence table.</span></span>

     

## <a name="tables-used-during-execution"></a><span data-ttu-id="2a42e-131">Tables utilisées lors de l’exécution</span><span class="sxs-lookup"><span data-stu-id="2a42e-131">Tables Used During Execution</span></span>

<span data-ttu-id="2a42e-132">La liste suivante identifie les tables utilisées lors de l’exécution :</span><span class="sxs-lookup"><span data-stu-id="2a42e-132">The following list identifies the tables that are used during execution:</span></span>

-   [<span data-ttu-id="2a42e-133">Table FeatureComponents</span><span class="sxs-lookup"><span data-stu-id="2a42e-133">FeatureComponents Table</span></span>](featurecomponents-table.md)
-   <span data-ttu-id="2a42e-134">\*Tables de séquence de module et tables de séquence correspondantes \* .</span><span class="sxs-lookup"><span data-stu-id="2a42e-134">Module\*Sequence tables and corresponding \*Sequence tables.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2a42e-135">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2a42e-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2a42e-136">À propos des modules de fusion</span><span class="sxs-lookup"><span data-stu-id="2a42e-136">About Merge Modules</span></span>](about-merge-modules.md)
</dt> <dt>

[<span data-ttu-id="2a42e-137">Référence ICE du module de fusion</span><span class="sxs-lookup"><span data-stu-id="2a42e-137">Merge Module ICE Reference</span></span>](merge-module-ice-reference.md)
</dt> </dl>

 

 



