---
description: ICEM03 vérifie que toutes les actions du module sont des actions de base ou qu’elles dérivent d’une action de base valide.
ms.assetid: 8e2b5921-32cf-45e8-9906-30002574a712
title: ICEM03
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f368fa50a71153c41eebaa9ee5084449cf824993
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534314"
---
# <a name="icem03"></a><span data-ttu-id="b70c9-103">ICEM03</span><span class="sxs-lookup"><span data-stu-id="b70c9-103">ICEM03</span></span>

<span data-ttu-id="b70c9-104">ICEM03 vérifie que toutes les actions du module sont des actions de base ou qu’elles dérivent d’une action de base valide.</span><span class="sxs-lookup"><span data-stu-id="b70c9-104">ICEM03 verifies that all actions in the module are either base actions or derive from a valid base action.</span></span>

<span data-ttu-id="b70c9-105">Le module de fusion CIEM est stocké dans un fichier de module de fusion. CUB appelé Mergemod. CUB et non dans le fichier. CUB contenant le CIEM utilisé pour la validation du package.</span><span class="sxs-lookup"><span data-stu-id="b70c9-105">Merge module ICEs are stored in a merge module .cub file called Mergemod.cub and not in the .cub file containing the ICEs used for package validation.</span></span>

## <a name="result"></a><span data-ttu-id="b70c9-106">Résultats</span><span class="sxs-lookup"><span data-stu-id="b70c9-106">Result</span></span>

<span data-ttu-id="b70c9-107">ICEM03 publie les messages d’erreur pour un module contenant des actions dans une table de séquences qui n’est pas une action de base ou qui est dérivée d’une action de base valide.</span><span class="sxs-lookup"><span data-stu-id="b70c9-107">ICEM03 posts the error messages for a module containing actions in a sequence table that is not a base action or derived from a valid base action.</span></span>

## <a name="example"></a><span data-ttu-id="b70c9-108">Exemple</span><span class="sxs-lookup"><span data-stu-id="b70c9-108">Example</span></span>

<span data-ttu-id="b70c9-109">ICEM03 publie les messages d’erreur suivants pour un module contenant les entrées de base de données présentées ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="b70c9-109">ICEM03 posts the following error messages for a module containing the database entries shown below.</span></span>

``` syntax
The action 'Action1' in the 'ModuleInstallExecuteSequence' table is 
orphaned. It is not a valid base action and does not derive from a 
valid base action.
The action 'Action2' in the 'ModuleInstallExecuteSequence' table is 
orphaned. It is not a valid base action and does not derive from a 
valid base action.
```

[<span data-ttu-id="b70c9-110">Table ModuleInstallExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="b70c9-110">ModuleInstallExecuteSequence Table</span></span>](moduleinstallexecutesequence-table.md)



| <span data-ttu-id="b70c9-111">Action</span><span class="sxs-lookup"><span data-stu-id="b70c9-111">Action</span></span>  | <span data-ttu-id="b70c9-112">Séquence</span><span class="sxs-lookup"><span data-stu-id="b70c9-112">Sequence</span></span> | <span data-ttu-id="b70c9-113">BaseAction</span><span class="sxs-lookup"><span data-stu-id="b70c9-113">BaseAction</span></span> | <span data-ttu-id="b70c9-114">After</span><span class="sxs-lookup"><span data-stu-id="b70c9-114">After</span></span> | <span data-ttu-id="b70c9-115">Condition</span><span class="sxs-lookup"><span data-stu-id="b70c9-115">Condition</span></span> |
|---------|----------|------------|-------|-----------|
| <span data-ttu-id="b70c9-116">Action1</span><span class="sxs-lookup"><span data-stu-id="b70c9-116">Action1</span></span> |          | <span data-ttu-id="b70c9-117">Action2</span><span class="sxs-lookup"><span data-stu-id="b70c9-117">Action2</span></span>    | <span data-ttu-id="b70c9-118">0</span><span class="sxs-lookup"><span data-stu-id="b70c9-118">0</span></span>     |           |
| <span data-ttu-id="b70c9-119">Action2</span><span class="sxs-lookup"><span data-stu-id="b70c9-119">Action2</span></span> |          | <span data-ttu-id="b70c9-120">Action1</span><span class="sxs-lookup"><span data-stu-id="b70c9-120">Action1</span></span>    | <span data-ttu-id="b70c9-121">0</span><span class="sxs-lookup"><span data-stu-id="b70c9-121">0</span></span>     |           |



 

<span data-ttu-id="b70c9-122">ICEM03 publie des erreurs pour ces deux actions, car elles font référence les unes aux autres comme des actions de base dans la table ModuleInstallExecuteSequence.</span><span class="sxs-lookup"><span data-stu-id="b70c9-122">ICEM03 posts errors for these two actions because they refer to each other as base actions in the ModuleInstallExecuteSequence table.</span></span> <span data-ttu-id="b70c9-123">Toutes les actions dans les tables [ModuleAdminUISequence](moduleadminuisequence-table.md), [ModuleAdminExecuteSequence](moduleadminexecutesequence-table.md), [ModuleAdvtUISequence](moduleadvtuisequence-table.md), [ModuleAdvtExecuteSequence](moduleadvtexecutesequence-table.md), [ModuleInstallUISequence](moduleinstalluisequence-table.md)et [ModuleInstallExecuteSequence](moduleinstallexecutesequence-table.md) doivent être des actions de base ou dériver leur position de la combinaison d’une autre action et d’un indicateur Before et after.</span><span class="sxs-lookup"><span data-stu-id="b70c9-123">All actions in the [ModuleAdminUISequence](moduleadminuisequence-table.md), [ModuleAdminExecuteSequence](moduleadminexecutesequence-table.md), [ModuleAdvtUISequence](moduleadvtuisequence-table.md), [ModuleAdvtExecuteSequence](moduleadvtexecutesequence-table.md), [ModuleInstallUISequence](moduleinstalluisequence-table.md), and [ModuleInstallExecuteSequence](moduleinstallexecutesequence-table.md) tables must either be base actions or derive their position from the combination of another action and a before and after flag.</span></span>

<span data-ttu-id="b70c9-124">Pour corriger cette erreur, déterminez les actions de base pour les deux actions.</span><span class="sxs-lookup"><span data-stu-id="b70c9-124">To fix this error, determine the base actions for the two actions.</span></span> <span data-ttu-id="b70c9-125">Ajoutez un enregistrement pour les actions de base avec un numéro de séquence par défaut.</span><span class="sxs-lookup"><span data-stu-id="b70c9-125">Add a record for the base actions with a default sequence number.</span></span> <span data-ttu-id="b70c9-126">Pour action1 et action2, entrez les noms des actions de base dans la colonne BaseAction et 0 ou 1 dans la colonne après.</span><span class="sxs-lookup"><span data-stu-id="b70c9-126">For Action1 and Action2 enter the base action names in the BaseAction column and 0 or 1 in the After column.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b70c9-127">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b70c9-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b70c9-128">Référence ICE du module de fusion</span><span class="sxs-lookup"><span data-stu-id="b70c9-128">Merge Module ICE Reference</span></span>](merge-module-ice-reference.md)
</dt> </dl>

 

 



