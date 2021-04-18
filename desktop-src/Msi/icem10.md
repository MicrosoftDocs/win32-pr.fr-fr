---
description: ICEM10 vérifie qu’un module de fusion contient uniquement des propriétés qui sont autorisées dans la table de propriétés.
ms.assetid: 9ac7a724-ea0e-4caa-bb4f-846bfb802037
title: ICEM10
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80263e5033ec14bd669c5d046c7f3842d58e332f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106533986"
---
# <a name="icem10"></a><span data-ttu-id="2da99-103">ICEM10</span><span class="sxs-lookup"><span data-stu-id="2da99-103">ICEM10</span></span>

<span data-ttu-id="2da99-104">ICEM10 vérifie qu’un module de fusion contient uniquement des propriétés qui sont autorisées dans la [table de propriétés](property-table.md).</span><span class="sxs-lookup"><span data-stu-id="2da99-104">ICEM10 verifies that a merge module contains only properties that are allowed in the [Property Table](property-table.md).</span></span> <span data-ttu-id="2da99-105">Les propriétés spécifiques au produit suivantes ne sont pas autorisées dans la table de propriétés :</span><span class="sxs-lookup"><span data-stu-id="2da99-105">The following product specific properties are not allowed in the Property Table:</span></span>

-   [<span data-ttu-id="2da99-106">**Propriété ProductLanguage**</span><span class="sxs-lookup"><span data-stu-id="2da99-106">**ProductLanguage Property**</span></span>](productlanguage.md)
-   [<span data-ttu-id="2da99-107">**Propriété ProductCode**</span><span class="sxs-lookup"><span data-stu-id="2da99-107">**ProductCode Property**</span></span>](productcode.md)
-   [<span data-ttu-id="2da99-108">**Propriété ProductVersion**</span><span class="sxs-lookup"><span data-stu-id="2da99-108">**ProductVersion Property**</span></span>](productversion.md)
-   [<span data-ttu-id="2da99-109">**Propriété ProductName**</span><span class="sxs-lookup"><span data-stu-id="2da99-109">**ProductName Property**</span></span>](productname.md)
-   [<span data-ttu-id="2da99-110">**Propriété Manufacturer**</span><span class="sxs-lookup"><span data-stu-id="2da99-110">**Manufacturer Property**</span></span>](manufacturer.md)

## <a name="result"></a><span data-ttu-id="2da99-111">Résultats</span><span class="sxs-lookup"><span data-stu-id="2da99-111">Result</span></span>

<span data-ttu-id="2da99-112">ICEM10 publie une erreur lorsqu’un module de fusion contient une propriété qui n’est pas autorisée dans la [table de propriétés](property-table.md).</span><span class="sxs-lookup"><span data-stu-id="2da99-112">ICEM10 posts an error when a merge module contains a property that is not allowed in the [Property Table](property-table.md).</span></span>

## <a name="example"></a><span data-ttu-id="2da99-113">Exemple</span><span class="sxs-lookup"><span data-stu-id="2da99-113">Example</span></span>

<span data-ttu-id="2da99-114">ICEM10 publie les messages d’erreur suivants pour un module qui contient les entrées de base de données affichées.</span><span class="sxs-lookup"><span data-stu-id="2da99-114">ICEM10 posts the following error messages for a module that contains the database entries shown.</span></span>

``` syntax
The property 'ProductLanguage' is not allowed in a merge module.

The property 'Manufacturer' is not allowed in a merge module.
```

<span data-ttu-id="2da99-115">Le tableau suivant présente une table de [Propriétés](property-table.md)partielle.</span><span class="sxs-lookup"><span data-stu-id="2da99-115">The following table shows you a partial [Property Table](property-table.md).</span></span>



| <span data-ttu-id="2da99-116">Propriété</span><span class="sxs-lookup"><span data-stu-id="2da99-116">Property</span></span>                                   | <span data-ttu-id="2da99-117">Valeurs</span><span class="sxs-lookup"><span data-stu-id="2da99-117">Values</span></span>    |
|--------------------------------------------|-----------|
| <span data-ttu-id="2da99-118">Couleur</span><span class="sxs-lookup"><span data-stu-id="2da99-118">Color</span></span>                                      | <span data-ttu-id="2da99-119">Rouge</span><span class="sxs-lookup"><span data-stu-id="2da99-119">Red</span></span>       |
| [<span data-ttu-id="2da99-120">**Fabricant**</span><span class="sxs-lookup"><span data-stu-id="2da99-120">**Manufacturer**</span></span>](manufacturer.md)       | <span data-ttu-id="2da99-121">Microsoft</span><span class="sxs-lookup"><span data-stu-id="2da99-121">Microsoft</span></span> |
| [<span data-ttu-id="2da99-122">**ProductLanguage**</span><span class="sxs-lookup"><span data-stu-id="2da99-122">**ProductLanguage**</span></span>](productlanguage.md) | <span data-ttu-id="2da99-123">1033</span><span class="sxs-lookup"><span data-stu-id="2da99-123">1033</span></span>      |



 

<span data-ttu-id="2da99-124">La procédure suivante vous montre comment corriger les erreurs.</span><span class="sxs-lookup"><span data-stu-id="2da99-124">The following procedure shows you how to fix errors.</span></span>

<span data-ttu-id="2da99-125">**Pour corriger les erreurs**</span><span class="sxs-lookup"><span data-stu-id="2da99-125">**To fix the errors**</span></span>

1.  <span data-ttu-id="2da99-126">Supprimez la propriété'[**Manufacturer**](manufacturer.md)'de la [table de propriétés](property-table.md).</span><span class="sxs-lookup"><span data-stu-id="2da99-126">Remove the '[**Manufacturer**](manufacturer.md)' property from the [Property Table](property-table.md).</span></span>
2.  <span data-ttu-id="2da99-127">Supprimez la propriété'[**ProductLanguage**](productlanguage.md)'de la [table de propriétés](property-table.md).</span><span class="sxs-lookup"><span data-stu-id="2da99-127">Remove the '[**ProductLanguage**](productlanguage.md)' property from the [Property Table](property-table.md).</span></span>

## <a name="table-used-during-execution"></a><span data-ttu-id="2da99-128">Table utilisée pendant l’exécution</span><span class="sxs-lookup"><span data-stu-id="2da99-128">Table Used During Execution</span></span>

<span data-ttu-id="2da99-129">La [table de propriétés](property-table.md) est utilisée lors de l’exécution.</span><span class="sxs-lookup"><span data-stu-id="2da99-129">The [Property Table](property-table.md) is used during execution.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2da99-130">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2da99-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2da99-131">Référence ICE du module de fusion</span><span class="sxs-lookup"><span data-stu-id="2da99-131">Merge Module ICE Reference</span></span>](merge-module-ice-reference.md)
</dt> </dl>

 

 



