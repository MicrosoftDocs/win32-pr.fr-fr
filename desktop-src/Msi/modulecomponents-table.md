---
description: La table ModuleComponents contient une liste des composants qui se trouvent dans le module de fusion.
ms.assetid: def96d52-c9fa-4fac-b575-f9de8eb82d1c
title: Table ModuleComponents
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ea2f47418b0387c7fa9d289d156fb0369f53adf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536822"
---
# <a name="modulecomponents-table"></a><span data-ttu-id="77a4d-103">Table ModuleComponents</span><span class="sxs-lookup"><span data-stu-id="77a4d-103">ModuleComponents Table</span></span>

<span data-ttu-id="77a4d-104">La table ModuleComponents contient une liste des composants qui se trouvent dans le module de fusion.</span><span class="sxs-lookup"><span data-stu-id="77a4d-104">The ModuleComponents table contains a list of the components found in the merge module.</span></span>

<span data-ttu-id="77a4d-105">La table ModuleComponents contient les colonnes suivantes.</span><span class="sxs-lookup"><span data-stu-id="77a4d-105">The ModuleComponents table has the following columns.</span></span>



| <span data-ttu-id="77a4d-106">Colonne</span><span class="sxs-lookup"><span data-stu-id="77a4d-106">Column</span></span>    | <span data-ttu-id="77a4d-107">Type</span><span class="sxs-lookup"><span data-stu-id="77a4d-107">Type</span></span>                         | <span data-ttu-id="77a4d-108">Clé</span><span class="sxs-lookup"><span data-stu-id="77a4d-108">Key</span></span> | <span data-ttu-id="77a4d-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="77a4d-109">Nullable</span></span> |
|-----------|------------------------------|-----|----------|
| <span data-ttu-id="77a4d-110">Composant</span><span class="sxs-lookup"><span data-stu-id="77a4d-110">Component</span></span> | [<span data-ttu-id="77a4d-111">Identificateur</span><span class="sxs-lookup"><span data-stu-id="77a4d-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="77a4d-112">O</span><span class="sxs-lookup"><span data-stu-id="77a4d-112">Y</span></span>   | <span data-ttu-id="77a4d-113">N</span><span class="sxs-lookup"><span data-stu-id="77a4d-113">N</span></span>        |
| <span data-ttu-id="77a4d-114">ModuleID</span><span class="sxs-lookup"><span data-stu-id="77a4d-114">ModuleID</span></span>  | [<span data-ttu-id="77a4d-115">Identificateur</span><span class="sxs-lookup"><span data-stu-id="77a4d-115">Identifier</span></span>](identifier.md) | <span data-ttu-id="77a4d-116">O</span><span class="sxs-lookup"><span data-stu-id="77a4d-116">Y</span></span>   | <span data-ttu-id="77a4d-117">N</span><span class="sxs-lookup"><span data-stu-id="77a4d-117">N</span></span>        |
| <span data-ttu-id="77a4d-118">Language</span><span class="sxs-lookup"><span data-stu-id="77a4d-118">Language</span></span>  | [<span data-ttu-id="77a4d-119">Integer</span><span class="sxs-lookup"><span data-stu-id="77a4d-119">Integer</span></span>](integer.md)       | <span data-ttu-id="77a4d-120">O</span><span class="sxs-lookup"><span data-stu-id="77a4d-120">Y</span></span>   | <span data-ttu-id="77a4d-121">N</span><span class="sxs-lookup"><span data-stu-id="77a4d-121">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="77a4d-122">Colonnes</span><span class="sxs-lookup"><span data-stu-id="77a4d-122">Columns</span></span>

<dl> <dt>

<span data-ttu-id="77a4d-123"><span id="Component"></span><span id="component"></span><span id="COMPONENT"></span>-</span><span class="sxs-lookup"><span data-stu-id="77a4d-123"><span id="Component"></span><span id="component"></span><span id="COMPONENT"></span>Component</span></span>
</dt> <dd>

<span data-ttu-id="77a4d-124">Identificateur qui fait référence à un composant dans le module de fusion.</span><span class="sxs-lookup"><span data-stu-id="77a4d-124">An identifier referring to a component in the merge module.</span></span> <span data-ttu-id="77a4d-125">La colonne de composant est une clé étrangère de la [table des composants](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="77a4d-125">The Component column is a foreign key to the [Component table](component-table.md).</span></span> <span data-ttu-id="77a4d-126">L’entrée dans la colonne de composant doit respecter la Convention d’affectation de noms pour [nommer les clés primaires dans les bases de données de module de fusion](naming-primary-keys-in-merge-module-databases.md).</span><span class="sxs-lookup"><span data-stu-id="77a4d-126">The entry in the Component column must follow the naming convention in [Naming Primary Keys in Merge Module Databases](naming-primary-keys-in-merge-module-databases.md).</span></span>

</dd> <dt>

<span data-ttu-id="77a4d-127"><span id="ModuleID"></span><span id="moduleid"></span><span id="MODULEID"></span>ModuleID</span><span class="sxs-lookup"><span data-stu-id="77a4d-127"><span id="ModuleID"></span><span id="moduleid"></span><span id="MODULEID"></span>ModuleID</span></span>
</dt> <dd>

<span data-ttu-id="77a4d-128">Identificateur du module de fusion.</span><span class="sxs-lookup"><span data-stu-id="77a4d-128">The identifier for the merge module.</span></span> <span data-ttu-id="77a4d-129">Il s’agit d’une clé étrangère de la [table ModuleSignature](modulesignature-table.md).</span><span class="sxs-lookup"><span data-stu-id="77a4d-129">This is a foreign key to the [ModuleSignature table](modulesignature-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="77a4d-130"><span id="Language"></span><span id="language"></span><span id="LANGUAGE"></span>Sous</span><span class="sxs-lookup"><span data-stu-id="77a4d-130"><span id="Language"></span><span id="language"></span><span id="LANGUAGE"></span>Language</span></span>
</dt> <dd>

<span data-ttu-id="77a4d-131">L’identificateur de langue décrit la langue par défaut pour le module de fusion.</span><span class="sxs-lookup"><span data-stu-id="77a4d-131">The Language identifier describes the default language for the merge module.</span></span> <span data-ttu-id="77a4d-132">L’identificateur de langue est au format décimal, par exemple, l’anglais des États-Unis est 1033.</span><span class="sxs-lookup"><span data-stu-id="77a4d-132">The language identifier is in decimal format, for example, U.S. English is 1033.</span></span> <span data-ttu-id="77a4d-133">Clé étrangère vers la [table ModuleSignature](modulesignature-table.md).</span><span class="sxs-lookup"><span data-stu-id="77a4d-133">Foreign key to the [ModuleSignature table](modulesignature-table.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="77a4d-134">Notes</span><span class="sxs-lookup"><span data-stu-id="77a4d-134">Remarks</span></span>

<span data-ttu-id="77a4d-135">Les transformations de langage doivent être en mesure de mettre à jour cette table si le module de fusion prend en charge plusieurs langues.</span><span class="sxs-lookup"><span data-stu-id="77a4d-135">Language transforms must be able to update this table if the merge module supports multiple languages.</span></span>

 

 



