---
description: Pendant une installation Windows Installer, le programme d’installation peut rechercher une entrée de Registre et créer une propriété contenant la valeur du Registre.
ms.assetid: 3a663fc7-cdcf-4ac3-8251-836ba0d3cc11
title: Recherche d’une entrée de Registre et création d’une propriété contenant la valeur du Registre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82bd7572c0176f4870eed199800715190d9bbbf9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862038"
---
# <a name="searching-for-a-registry-entry-and-creating-a-property-holding-the-value-of-the-registry"></a><span data-ttu-id="ae28d-103">Recherche d’une entrée de Registre et création d’une propriété contenant la valeur du Registre</span><span class="sxs-lookup"><span data-stu-id="ae28d-103">Searching for a Registry Entry and Creating a Property Holding the Value of the Registry</span></span>

<span data-ttu-id="ae28d-104">**Pour rechercher une entrée de Registre et créer une propriété contenant la valeur de ce fichier**</span><span class="sxs-lookup"><span data-stu-id="ae28d-104">**To search for a registry entry and create a property holding the value of that file**</span></span>

1.  <span data-ttu-id="ae28d-105">N’ajoutez pas la signature à la table de [signature](signature-table.md) ou à la [table CompLocator](complocator-table.md).</span><span class="sxs-lookup"><span data-stu-id="ae28d-105">Do not add the signature to the [Signature Table](signature-table.md) or the [CompLocator Table](complocator-table.md).</span></span> <span data-ttu-id="ae28d-106">Si une signature de fichier figure dans la [table AppSearch](appsearch-table.md) et qu’elle n’est pas listée dans les tables signature ou CompLocator, le programme d’installation recherche dans la [table RegLocator](reglocator-table.md).</span><span class="sxs-lookup"><span data-stu-id="ae28d-106">If a file signature is listed in the [AppSearch Table](appsearch-table.md) and is not listed in the Signature or CompLocator tables, the Installer looks in the [RegLocator Table](reglocator-table.md).</span></span>

2.  <span data-ttu-id="ae28d-107">Spécifiez l’entrée de Registre à rechercher dans la [table RegLocator](reglocator-table.md).</span><span class="sxs-lookup"><span data-stu-id="ae28d-107">Specify the registry entry to be searched for in the [RegLocator Table](reglocator-table.md).</span></span> <span data-ttu-id="ae28d-108">Si la signature est absente de la [table de signature](signature-table.md) et que la valeur de la colonne de type est **msidbLocatorTypeRawValue**, la recherche est supposée être pour le nom de clé de Registre spécifique vers lequel pointe la table RegLocator.</span><span class="sxs-lookup"><span data-stu-id="ae28d-108">If the signature is absent from the [Signature Table](signature-table.md) and the value of the Type column is **msidbLocatorTypeRawValue**, then the search is assumed to be for the specific registry key name pointed to by the RegLocator Table.</span></span>

    <span data-ttu-id="ae28d-109">[Table RegLocator](reglocator-table.md) (partielle)</span><span class="sxs-lookup"><span data-stu-id="ae28d-109">[RegLocator Table](reglocator-table.md) (partial)</span></span>

    

    | <span data-ttu-id="ae28d-110">Signature\_</span><span class="sxs-lookup"><span data-stu-id="ae28d-110">Signature\_</span></span>         | <span data-ttu-id="ae28d-111">Root</span><span class="sxs-lookup"><span data-stu-id="ae28d-111">Root</span></span>         | <span data-ttu-id="ae28d-112">Clé</span><span class="sxs-lookup"><span data-stu-id="ae28d-112">Key</span></span>                                                           | <span data-ttu-id="ae28d-113">Nom</span><span class="sxs-lookup"><span data-stu-id="ae28d-113">Name</span></span>                  | <span data-ttu-id="ae28d-114">Type</span><span class="sxs-lookup"><span data-stu-id="ae28d-114">Type</span></span>                                    |
    |---------------------|--------------|---------------------------------------------------------------|-----------------------|-----------------------------------------|
    | <span data-ttu-id="ae28d-115">AppValue</span><span class="sxs-lookup"><span data-stu-id="ae28d-115">AppValue</span></span><br/> | <span data-ttu-id="ae28d-116">2</span><span class="sxs-lookup"><span data-stu-id="ae28d-116">2</span></span><br/> | <span data-ttu-id="ae28d-117">**Logiciel** \\ **Microsoft** \\ **MyApp**</span><span class="sxs-lookup"><span data-stu-id="ae28d-117">**SOFTWARE**\\**Microsoft**\\**MyApp**</span></span><br/> <br/> | <span data-ttu-id="ae28d-118">**SOCIETE**</span><span class="sxs-lookup"><span data-stu-id="ae28d-118">**Myname**</span></span><br/> | <span data-ttu-id="ae28d-119">**msidbLocatorTypeRawValue**</span><span class="sxs-lookup"><span data-stu-id="ae28d-119">**msidbLocatorTypeRawValue**</span></span><br/> |

    

     

3.  <span data-ttu-id="ae28d-120">Enfin, remplissez la [table AppSearch](appsearch-table.md) afin que l' [action AppSearch](appsearch-action.md) retourne la valeur de AppValue.</span><span class="sxs-lookup"><span data-stu-id="ae28d-120">Finally, populate the [AppSearch Table](appsearch-table.md) so that the [AppSearch Action](appsearch-action.md) returns the value of AppValue.</span></span> <span data-ttu-id="ae28d-121">Une fois que le programme d’installation a exécuté l’action AppSearch, la valeur de MYREGVAL est la valeur de AppValue.</span><span class="sxs-lookup"><span data-stu-id="ae28d-121">After the Installer executes the AppSearch Action, the value of MYREGVAL is the value of AppValue.</span></span>

    <span data-ttu-id="ae28d-122">[Table AppSearch](appsearch-table.md) (partielle)</span><span class="sxs-lookup"><span data-stu-id="ae28d-122">[AppSearch Table](appsearch-table.md) (partial)</span></span>

    

    | <span data-ttu-id="ae28d-123">Propriété</span><span class="sxs-lookup"><span data-stu-id="ae28d-123">Property</span></span>            | <span data-ttu-id="ae28d-124">Signature</span><span class="sxs-lookup"><span data-stu-id="ae28d-124">Signature</span></span>           |
    |---------------------|---------------------|
    | <span data-ttu-id="ae28d-125">MYREGVAL</span><span class="sxs-lookup"><span data-stu-id="ae28d-125">MYREGVAL</span></span><br/> | <span data-ttu-id="ae28d-126">AppValue</span><span class="sxs-lookup"><span data-stu-id="ae28d-126">AppValue</span></span><br/> |

    

     

 

 




