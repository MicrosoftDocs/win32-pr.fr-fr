---
description: La table FeatureComponents définit la relation entre les fonctionnalités et les composants. Pour chaque fonctionnalité, ce tableau répertorie tous les composants qui composent cette fonctionnalité.
ms.assetid: aff16483-a9ed-4675-8e87-8adf695605ee
title: Table FeatureComponents
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6c93a7c020f179843916b063b48e2e4d19f7bf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103754228"
---
# <a name="featurecomponents-table"></a><span data-ttu-id="9b156-104">Table FeatureComponents</span><span class="sxs-lookup"><span data-stu-id="9b156-104">FeatureComponents Table</span></span>

<span data-ttu-id="9b156-105">La table FeatureComponents définit la relation entre les fonctionnalités et les composants.</span><span class="sxs-lookup"><span data-stu-id="9b156-105">The FeatureComponents table defines the relationship between features and components.</span></span> <span data-ttu-id="9b156-106">Pour chaque fonctionnalité, ce tableau répertorie tous les composants qui composent cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="9b156-106">For each feature, this table lists all the components that make up that feature.</span></span>

<span data-ttu-id="9b156-107">La table FeatureComponents contient les colonnes suivantes.</span><span class="sxs-lookup"><span data-stu-id="9b156-107">The FeatureComponents table has the following columns.</span></span>



| <span data-ttu-id="9b156-108">Colonne</span><span class="sxs-lookup"><span data-stu-id="9b156-108">Column</span></span>      | <span data-ttu-id="9b156-109">Type</span><span class="sxs-lookup"><span data-stu-id="9b156-109">Type</span></span>                         | <span data-ttu-id="9b156-110">Clé</span><span class="sxs-lookup"><span data-stu-id="9b156-110">Key</span></span> | <span data-ttu-id="9b156-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="9b156-111">Nullable</span></span> |
|-------------|------------------------------|-----|----------|
| <span data-ttu-id="9b156-112">Fonctionnalité\_</span><span class="sxs-lookup"><span data-stu-id="9b156-112">Feature\_</span></span>   | [<span data-ttu-id="9b156-113">Identificateur</span><span class="sxs-lookup"><span data-stu-id="9b156-113">Identifier</span></span>](identifier.md) | <span data-ttu-id="9b156-114">O</span><span class="sxs-lookup"><span data-stu-id="9b156-114">Y</span></span>   | <span data-ttu-id="9b156-115">N</span><span class="sxs-lookup"><span data-stu-id="9b156-115">N</span></span>        |
| <span data-ttu-id="9b156-116">-\_</span><span class="sxs-lookup"><span data-stu-id="9b156-116">Component\_</span></span> | [<span data-ttu-id="9b156-117">Identificateur</span><span class="sxs-lookup"><span data-stu-id="9b156-117">Identifier</span></span>](identifier.md) | <span data-ttu-id="9b156-118">O</span><span class="sxs-lookup"><span data-stu-id="9b156-118">Y</span></span>   | <span data-ttu-id="9b156-119">N</span><span class="sxs-lookup"><span data-stu-id="9b156-119">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="9b156-120">Colonnes</span><span class="sxs-lookup"><span data-stu-id="9b156-120">Columns</span></span>

<dl> <dt>

<span data-ttu-id="9b156-121"><span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Fonctionnalité\_</span><span class="sxs-lookup"><span data-stu-id="9b156-121"><span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Feature\_</span></span>
</dt> <dd>

<span data-ttu-id="9b156-122">Clé externe dans la première colonne de la [table](feature-table.md)de fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="9b156-122">An external key into the first column of the Feature [table](feature-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="9b156-123"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>-\_</span><span class="sxs-lookup"><span data-stu-id="9b156-123"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="9b156-124">Clé externe dans la première colonne de la [table de composants](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="9b156-124">An external key into the first column of the [Component table](component-table.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9b156-125">Notes</span><span class="sxs-lookup"><span data-stu-id="9b156-125">Remarks</span></span>

<span data-ttu-id="9b156-126">Il existe une limite maximale de 1600 composants par fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="9b156-126">There is a maximum limit of 1600 components per feature.</span></span>

<span data-ttu-id="9b156-127">Les composants peuvent être partagés par plusieurs fonctionnalités, autrement dit, un même composant peut être référencé par plusieurs fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="9b156-127">Components can be shared by two or more features, that is, the same component can be referred to by more than one feature.</span></span>

<span data-ttu-id="9b156-128">Cette table est référencée lorsque l' [action PublishFeatures](publishfeatures-action.md) ou l' [action UnpublishFeatures](unpublishfeatures-action.md) est exécutée.</span><span class="sxs-lookup"><span data-stu-id="9b156-128">This table is referred to when the [PublishFeatures action](publishfeatures-action.md) or the [UnpublishFeatures action](unpublishfeatures-action.md) is executed.</span></span>

## <a name="validation"></a><span data-ttu-id="9b156-129">Validation</span><span class="sxs-lookup"><span data-stu-id="9b156-129">Validation</span></span>

<dl>

[<span data-ttu-id="9b156-130">ICE03</span><span class="sxs-lookup"><span data-stu-id="9b156-130">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="9b156-131">ICE06</span><span class="sxs-lookup"><span data-stu-id="9b156-131">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="9b156-132">ICE21</span><span class="sxs-lookup"><span data-stu-id="9b156-132">ICE21</span></span>](ice21.md)  
[<span data-ttu-id="9b156-133">ICE22</span><span class="sxs-lookup"><span data-stu-id="9b156-133">ICE22</span></span>](ice22.md)  
[<span data-ttu-id="9b156-134">ICE32</span><span class="sxs-lookup"><span data-stu-id="9b156-134">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="9b156-135">ICE41</span><span class="sxs-lookup"><span data-stu-id="9b156-135">ICE41</span></span>](ice41.md)  
[<span data-ttu-id="9b156-136">ICE47</span><span class="sxs-lookup"><span data-stu-id="9b156-136">ICE47</span></span>](ice47.md)  
[<span data-ttu-id="9b156-137">ICE59</span><span class="sxs-lookup"><span data-stu-id="9b156-137">ICE59</span></span>](ice59.md)  
[<span data-ttu-id="9b156-138">ICE62</span><span class="sxs-lookup"><span data-stu-id="9b156-138">ICE62</span></span>](ice62.md)  
[<span data-ttu-id="9b156-139">ICE69</span><span class="sxs-lookup"><span data-stu-id="9b156-139">ICE69</span></span>](ice69.md)  
</dl>

 

 



