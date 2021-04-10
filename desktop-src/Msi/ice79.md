---
description: ICE79 valide les références aux composants et aux fonctionnalités entrées dans les champs de la base de données à l’aide du type de données condition.
ms.assetid: f0a8ceac-084a-4693-b27d-f610eec4702a
title: ICE79
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9081297f2bf2f11283380c0f057bd0fbec417975
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113850"
---
# <a name="ice79"></a><span data-ttu-id="bdd45-103">ICE79</span><span class="sxs-lookup"><span data-stu-id="bdd45-103">ICE79</span></span>

<span data-ttu-id="bdd45-104">ICE79 valide les références aux composants et aux fonctionnalités entrées dans les champs de la base de données à l’aide du type de données [condition](condition.md) .</span><span class="sxs-lookup"><span data-stu-id="bdd45-104">ICE79 validates the references to components and features entered in the database fields using the [Condition](condition.md) data type.</span></span>

## <a name="result"></a><span data-ttu-id="bdd45-105">Résultats</span><span class="sxs-lookup"><span data-stu-id="bdd45-105">Result</span></span>

<span data-ttu-id="bdd45-106">ICE79 publie deux avertissements.</span><span class="sxs-lookup"><span data-stu-id="bdd45-106">ICE79 posts two warnings.</span></span>



| <span data-ttu-id="bdd45-107">AVERTISSEMENT ICE79</span><span class="sxs-lookup"><span data-stu-id="bdd45-107">ICE79 warning</span></span>                                                                      | <span data-ttu-id="bdd45-108">Description</span><span class="sxs-lookup"><span data-stu-id="bdd45-108">Description</span></span>                                                      |
|------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span data-ttu-id="bdd45-109">La base de données ne contient pas de \_ table de validation.</span><span class="sxs-lookup"><span data-stu-id="bdd45-109">Database is missing \_Validation table.</span></span> <span data-ttu-id="bdd45-110">Impossible de vérifier complètement les noms de propriété.</span><span class="sxs-lookup"><span data-stu-id="bdd45-110">Could not completely check property names.</span></span> | <span data-ttu-id="bdd45-111">La base de données ne contient pas de [ \_ table de validation](-validation-table.md).</span><span class="sxs-lookup"><span data-stu-id="bdd45-111">Database is missing [\_Validation table](-validation-table.md).</span></span> |
| <span data-ttu-id="bdd45-112">Erreur lors de la récupération des valeurs de la colonne \[ 2 \] du tableau \[ 1 \] .</span><span class="sxs-lookup"><span data-stu-id="bdd45-112">Error retrieving values from column \[2\] in table \[1\].</span></span> <span data-ttu-id="bdd45-113">Colonne ignorée.</span><span class="sxs-lookup"><span data-stu-id="bdd45-113">Skipping Column.</span></span>         | <span data-ttu-id="bdd45-114">Erreur lors de la récupération de la valeur.</span><span class="sxs-lookup"><span data-stu-id="bdd45-114">Error retrieving value.</span></span>                                          |



 

<span data-ttu-id="bdd45-115">ICE79 publie deux erreurs.</span><span class="sxs-lookup"><span data-stu-id="bdd45-115">ICE79 posts two errors.</span></span>



| <span data-ttu-id="bdd45-116">Erreur ICE79</span><span class="sxs-lookup"><span data-stu-id="bdd45-116">ICE79 error</span></span>                                                          | <span data-ttu-id="bdd45-117">Description</span><span class="sxs-lookup"><span data-stu-id="bdd45-117">Description</span></span>                               |
|----------------------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="bdd45-118">Composant'% ls’référencé dans la colonne'% s'. ' % s’de la ligne% s n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="bdd45-118">Component '%ls' referenced in column '%s'.'%s' of row %s is invalid.</span></span> | <span data-ttu-id="bdd45-119">Une référence de composant non valide a été trouvée.</span><span class="sxs-lookup"><span data-stu-id="bdd45-119">An invalid component reference was found.</span></span> |
| <span data-ttu-id="bdd45-120">La fonctionnalité'% ls’est référencée dans la colonne'% s'. ' % s’de la ligne% s n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="bdd45-120">Feature '%ls' referenced in column '%s'.'%s' of row %s is invalid.</span></span>   | <span data-ttu-id="bdd45-121">Une référence de fonctionnalité non valide a été trouvée</span><span class="sxs-lookup"><span data-stu-id="bdd45-121">An invalid feature reference was found</span></span>    |



 

## <a name="example"></a><span data-ttu-id="bdd45-122">Exemple</span><span class="sxs-lookup"><span data-stu-id="bdd45-122">Example</span></span>

<span data-ttu-id="bdd45-123">ICE79 signale les erreurs suivantes pour l’exemple :</span><span class="sxs-lookup"><span data-stu-id="bdd45-123">ICE79 reports the following errors for the example:</span></span>

``` syntax
Component 'NoSuchComponent' referenced in column 
'InstallExecuteSequence'.'Condition' of row Custom2 is invalid.
Feature 'NoSuchFeature' referenced in column 
'InstallExecuteSequence'.'Condition' of row Custom1 is invalid.
```

<span data-ttu-id="bdd45-124">Dans cet exemple, NoSuchComponent est absent de la [table Component](component-table.md) et NoSuchFeature est absent de la [table Feature](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="bdd45-124">In this example, NoSuchComponent is absent from the [Component table](component-table.md) and NoSuchFeature is absent from the [Feature table](feature-table.md).</span></span>

<span data-ttu-id="bdd45-125">[Table InstallExecuteSequence](installexecutesequence-table.md) (partielle)</span><span class="sxs-lookup"><span data-stu-id="bdd45-125">[InstallExecuteSequence Table](installexecutesequence-table.md) (partial)</span></span>



| <span data-ttu-id="bdd45-126">Action</span><span class="sxs-lookup"><span data-stu-id="bdd45-126">Action</span></span>  | <span data-ttu-id="bdd45-127">Condition</span><span class="sxs-lookup"><span data-stu-id="bdd45-127">Condition</span></span>                                |
|---------|------------------------------------------|
| <span data-ttu-id="bdd45-128">CUSTOM1</span><span class="sxs-lookup"><span data-stu-id="bdd45-128">Custom1</span></span> | <span data-ttu-id="bdd45-129">TESTACTION = 1046 et &NoSuchFeature>2</span><span class="sxs-lookup"><span data-stu-id="bdd45-129">TESTACTION=1046 AND &NoSuchFeature>2</span></span>  |
| <span data-ttu-id="bdd45-130">CUSTOM2</span><span class="sxs-lookup"><span data-stu-id="bdd45-130">Custom2</span></span> | <span data-ttu-id="bdd45-131">TESTACTION = 146 et $NoSuchComponent>2</span><span class="sxs-lookup"><span data-stu-id="bdd45-131">TESTACTION=146 AND $NoSuchComponent>2</span></span> |



 

<span data-ttu-id="bdd45-132">Pour corriger ces erreurs, entrez des enregistrements valides pour NoSuchFeature et NoSuchComponent dans les tables des fonctionnalités et des composants.</span><span class="sxs-lookup"><span data-stu-id="bdd45-132">To fix these errors, enter valid records for NoSuchFeature and NoSuchComponent in the Feature and Component tables.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bdd45-133">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="bdd45-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bdd45-134">Référence ICE</span><span class="sxs-lookup"><span data-stu-id="bdd45-134">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



