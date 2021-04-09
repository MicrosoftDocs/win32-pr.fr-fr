---
description: ICEM05 vérifie que le module de fusion est correctement associé aux composants dans le module. Si vous associez de manière incorrecte un composant à un module, le composant n’est pas correctement associé à la base de données cible.
ms.assetid: 1bf4041e-b198-4897-8719-8505fd8180ec
title: ICEM05
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e62ca481ef836c2675c381817fe2242e37384818
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034400"
---
# <a name="icem05"></a><span data-ttu-id="22eb4-104">ICEM05</span><span class="sxs-lookup"><span data-stu-id="22eb4-104">ICEM05</span></span>

<span data-ttu-id="22eb4-105">ICEM05 vérifie que le module de fusion est correctement associé aux composants dans le module.</span><span class="sxs-lookup"><span data-stu-id="22eb4-105">ICEM05 verifies that the merge module is correctly associated with components in the module.</span></span> <span data-ttu-id="22eb4-106">Si vous associez de manière incorrecte un composant à un module, le composant n’est pas correctement associé à la base de données cible.</span><span class="sxs-lookup"><span data-stu-id="22eb4-106">Incorrectly associating a component with a module causes the component to be incorrectly associated with the target database.</span></span>

<span data-ttu-id="22eb4-107">Le module de fusion CIEM est stocké dans un fichier de module de fusion. CUB appelé Mergemod. CUB et non dans le fichier. CUB contenant le CIEM utilisé pour la validation du package.</span><span class="sxs-lookup"><span data-stu-id="22eb4-107">Merge module ICEs are stored in a merge module .cub file called Mergemod.cub and not in the .cub file containing the ICEs used for package validation.</span></span>

## <a name="result"></a><span data-ttu-id="22eb4-108">Résultats</span><span class="sxs-lookup"><span data-stu-id="22eb4-108">Result</span></span>

<span data-ttu-id="22eb4-109">ICEM05 publie une erreur si la base de données du module associe de manière incorrecte des composants et le module.</span><span class="sxs-lookup"><span data-stu-id="22eb4-109">ICEM05 posts an error if the module database incorrectly associates components and the module.</span></span>

## <a name="example"></a><span data-ttu-id="22eb4-110">Exemple</span><span class="sxs-lookup"><span data-stu-id="22eb4-110">Example</span></span>

<span data-ttu-id="22eb4-111">ICEM05 publie les messages d’erreur suivants pour un module contenant les entrées de base de données présentées ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="22eb4-111">ICEM05 posts the following error messages for a module containing the database entries shown below.</span></span>

``` syntax
The component Component2.OtherModule.GUID2.1033 in the 
ModuleComponents table does not belong to this Merge Module.
The component Component1.MyModule.GUID1.1033 in the ModuleComponents 
table is not listed in the Component table.
The component 'Component3' in the Component table is not listed in the 
ModuleComponents table.
```

[<span data-ttu-id="22eb4-112">ModuleSignature, table</span><span class="sxs-lookup"><span data-stu-id="22eb4-112">ModuleSignature Table</span></span>](modulesignature-table.md)



| <span data-ttu-id="22eb4-113">ModuleID</span><span class="sxs-lookup"><span data-stu-id="22eb4-113">ModuleID</span></span>         | <span data-ttu-id="22eb4-114">Langage</span><span class="sxs-lookup"><span data-stu-id="22eb4-114">Language</span></span> | <span data-ttu-id="22eb4-115">Version</span><span class="sxs-lookup"><span data-stu-id="22eb4-115">Version</span></span> |
|------------------|----------|---------|
| <span data-ttu-id="22eb4-116">MyModule. *Guid1*</span><span class="sxs-lookup"><span data-stu-id="22eb4-116">MyModule.*GUID1*</span></span> | <span data-ttu-id="22eb4-117">1033</span><span class="sxs-lookup"><span data-stu-id="22eb4-117">1033</span></span>     | <span data-ttu-id="22eb4-118">1.0</span><span class="sxs-lookup"><span data-stu-id="22eb4-118">1.0</span></span>     |



 

[<span data-ttu-id="22eb4-119">**Table ModuleComponents**</span><span class="sxs-lookup"><span data-stu-id="22eb4-119">**ModuleComponents Table**</span></span>](modulecomponents-table.md)



| <span data-ttu-id="22eb4-120">Composant</span><span class="sxs-lookup"><span data-stu-id="22eb4-120">Component</span></span>  | <span data-ttu-id="22eb4-121">ModuleID</span><span class="sxs-lookup"><span data-stu-id="22eb4-121">ModuleID</span></span>            | <span data-ttu-id="22eb4-122">Language</span><span class="sxs-lookup"><span data-stu-id="22eb4-122">Language</span></span> |
|------------|---------------------|----------|
| <span data-ttu-id="22eb4-123">Composant1</span><span class="sxs-lookup"><span data-stu-id="22eb4-123">Component1</span></span> | <span data-ttu-id="22eb4-124">MyModule. *Guid1*</span><span class="sxs-lookup"><span data-stu-id="22eb4-124">MyModule.*GUID1*</span></span>    | <span data-ttu-id="22eb4-125">1033</span><span class="sxs-lookup"><span data-stu-id="22eb4-125">1033</span></span>     |
| <span data-ttu-id="22eb4-126">Component2</span><span class="sxs-lookup"><span data-stu-id="22eb4-126">Component2</span></span> | <span data-ttu-id="22eb4-127">OtherModule. *GUID2*</span><span class="sxs-lookup"><span data-stu-id="22eb4-127">OtherModule.*GUID2*</span></span> | <span data-ttu-id="22eb4-128">1033</span><span class="sxs-lookup"><span data-stu-id="22eb4-128">1033</span></span>     |



 

<span data-ttu-id="22eb4-129">[Table des composants](component-table.md) (partielle)</span><span class="sxs-lookup"><span data-stu-id="22eb4-129">[Component Table](component-table.md) (partial)</span></span>



| <span data-ttu-id="22eb4-130">Composant</span><span class="sxs-lookup"><span data-stu-id="22eb4-130">Component</span></span>  | <span data-ttu-id="22eb4-131">ComponentID</span><span class="sxs-lookup"><span data-stu-id="22eb4-131">ComponentID</span></span> |
|------------|-------------|
| <span data-ttu-id="22eb4-132">Component3</span><span class="sxs-lookup"><span data-stu-id="22eb4-132">Component3</span></span> | <span data-ttu-id="22eb4-133">*GUID4*</span><span class="sxs-lookup"><span data-stu-id="22eb4-133">*GUID4*</span></span>     |
| <span data-ttu-id="22eb4-134">Component2</span><span class="sxs-lookup"><span data-stu-id="22eb4-134">Component2</span></span> | <span data-ttu-id="22eb4-135">*GUID5*</span><span class="sxs-lookup"><span data-stu-id="22eb4-135">*GUID5*</span></span>     |



 

<span data-ttu-id="22eb4-136">Le module de fusion ICE signale la première erreur, car la table ModuleComponents tente d’associer un composant à un autre module qui n’est pas le module en cours spécifié dans la table ModuleSignature.</span><span class="sxs-lookup"><span data-stu-id="22eb4-136">The merge module ICE reports the first error because the ModuleComponents table attempts to associate a component with another module that is not the current module specified in the ModuleSignature table.</span></span> <span data-ttu-id="22eb4-137">Pour résoudre ce problème, remplacez les colonnes ModuleID et Language de l’enregistrement ModuleComponents pour COMPONENT2 par celles du module actuel, MyModule. *Guid1*.</span><span class="sxs-lookup"><span data-stu-id="22eb4-137">To fix this, change the ModuleID and Language columns of the ModuleComponents record for Component2 to that for the current module, MyModule.*GUID1*.</span></span>

<span data-ttu-id="22eb4-138">Le module de fusion ICE signale la deuxième erreur, car le premier enregistrement de la table ModuleComponents tente d’associer Composant1 au module.</span><span class="sxs-lookup"><span data-stu-id="22eb4-138">The merge module ICE reports the second error because the first record in the ModuleComponents table attempts to associate Component1 with the module.</span></span> <span data-ttu-id="22eb4-139">Ce composant n’existe pas dans la table des composants du module de fusion.</span><span class="sxs-lookup"><span data-stu-id="22eb4-139">This component does not exist in the Component Table of the merge module.</span></span> <span data-ttu-id="22eb4-140">Un module ne peut être associé qu’à un composant qui existe dans le module.</span><span class="sxs-lookup"><span data-stu-id="22eb4-140">A module can only be associated with a component that exists in the module.</span></span> <span data-ttu-id="22eb4-141">Pour résoudre ce problème, supprimez l’enregistrement du composant inexistant.</span><span class="sxs-lookup"><span data-stu-id="22eb4-141">To fix this, remove the record for the non-existent component.</span></span>

<span data-ttu-id="22eb4-142">Le module de fusion ICE signale la troisième erreur, car le module tente d’ajouter Component3 à la base de données cible.</span><span class="sxs-lookup"><span data-stu-id="22eb4-142">The merge module ICE reports the third error because the module attempts to add Component3 to the target database.</span></span> <span data-ttu-id="22eb4-143">Ce composant n’a pas été associé au module dans la table ModuleComponents.</span><span class="sxs-lookup"><span data-stu-id="22eb4-143">This component has not been associated with the module in the ModuleComponents table.</span></span> <span data-ttu-id="22eb4-144">Pour corriger cette erreur, ajoutez un enregistrement pour Component3 à la table ModuleComponents.</span><span class="sxs-lookup"><span data-stu-id="22eb4-144">To fix this error, add a record for Component3 to the ModuleComponents table.</span></span>

## <a name="related-topics"></a><span data-ttu-id="22eb4-145">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="22eb4-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="22eb4-146">Référence ICE du module de fusion</span><span class="sxs-lookup"><span data-stu-id="22eb4-146">Merge Module ICE Reference</span></span>](merge-module-ice-reference.md)
</dt> </dl>

 

 



