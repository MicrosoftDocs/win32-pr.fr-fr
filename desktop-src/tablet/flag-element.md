---
description: Contient une bitmap encodée en base64 d’un indicateur associé à la section d’une note du journal.
ms.assetid: 612f8814-ab3c-4a3e-9791-525788d4cc72
title: Flag, élément
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b6eda9aeb29c07c0de05eadffb8ba8d60f81954
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106536973"
---
# <a name="flag-element"></a><span data-ttu-id="3d6c9-103">Flag, élément</span><span class="sxs-lookup"><span data-stu-id="3d6c9-103">Flag Element</span></span>

<span data-ttu-id="3d6c9-104">Contient une bitmap encodée en base64 d’un indicateur associé à la section d’une note du journal.</span><span class="sxs-lookup"><span data-stu-id="3d6c9-104">Contains a base64 encoded bitmap of a flag associated with section of a Journal note.</span></span>

## <a name="definition"></a><span data-ttu-id="3d6c9-105">Définition</span><span class="sxs-lookup"><span data-stu-id="3d6c9-105">Definition</span></span>

``` syntax
<xs:element name="Flag" type="FlagType" minOccurs="0" maxOccurs="unbounded" />
```

## <a name="parent-elements"></a><span data-ttu-id="3d6c9-106">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="3d6c9-106">Parent Elements</span></span>

[<span data-ttu-id="3d6c9-107">**Content**</span><span class="sxs-lookup"><span data-stu-id="3d6c9-107">**Content**</span></span>](content-element--journal-reader.md)

[<span data-ttu-id="3d6c9-108">**, Nœud**</span><span class="sxs-lookup"><span data-stu-id="3d6c9-108">**GroupNode**</span></span>](groupnode-element.md)

## <a name="child-elements"></a><span data-ttu-id="3d6c9-109">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="3d6c9-109">Child Elements</span></span>

<span data-ttu-id="3d6c9-110">Aucun</span><span class="sxs-lookup"><span data-stu-id="3d6c9-110">None.</span></span>

## <a name="attributes"></a><span data-ttu-id="3d6c9-111">Attributs</span><span class="sxs-lookup"><span data-stu-id="3d6c9-111">Attributes</span></span>



| <span data-ttu-id="3d6c9-112">Attribut</span><span class="sxs-lookup"><span data-stu-id="3d6c9-112">Attribute</span></span>  | <span data-ttu-id="3d6c9-113">Type</span><span class="sxs-lookup"><span data-stu-id="3d6c9-113">Type</span></span>                      | <span data-ttu-id="3d6c9-114">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="3d6c9-114">Required</span></span> | <span data-ttu-id="3d6c9-115">Description</span><span class="sxs-lookup"><span data-stu-id="3d6c9-115">Description</span></span>                                                                             | <span data-ttu-id="3d6c9-116">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="3d6c9-116">Possible Values</span></span>           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| <span data-ttu-id="3d6c9-117">**Left**</span><span class="sxs-lookup"><span data-stu-id="3d6c9-117">**Left**</span></span>   | <span data-ttu-id="3d6c9-118">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="3d6c9-118">**xs:integer**</span></span>            | <span data-ttu-id="3d6c9-119">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="3d6c9-119">Required</span></span> | <span data-ttu-id="3d6c9-120">Distance entre l’origine et le point le plus à gauche dans le cadre englobant de l’élément.</span><span class="sxs-lookup"><span data-stu-id="3d6c9-120">The distance from the origin to the leftmost point in the bounding box for the element.</span></span> | <span data-ttu-id="3d6c9-121">N’importe quel entier.</span><span class="sxs-lookup"><span data-stu-id="3d6c9-121">Any integer.</span></span>              |
| <span data-ttu-id="3d6c9-122">**Top**</span><span class="sxs-lookup"><span data-stu-id="3d6c9-122">**Top**</span></span>    | <span data-ttu-id="3d6c9-123">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="3d6c9-123">**xs:integer**</span></span>            | <span data-ttu-id="3d6c9-124">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="3d6c9-124">Required</span></span> | <span data-ttu-id="3d6c9-125">Distance entre l’origine et le point le plus élevé dans le cadre englobant de l’élément.</span><span class="sxs-lookup"><span data-stu-id="3d6c9-125">The distance from the origin to the topmost point in the bounding box for the element.</span></span>  | <span data-ttu-id="3d6c9-126">N’importe quel entier.</span><span class="sxs-lookup"><span data-stu-id="3d6c9-126">Any integer.</span></span>              |
| <span data-ttu-id="3d6c9-127">**Width**</span><span class="sxs-lookup"><span data-stu-id="3d6c9-127">**Width**</span></span>  | <span data-ttu-id="3d6c9-128">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="3d6c9-128">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="3d6c9-129">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="3d6c9-129">Required</span></span> | <span data-ttu-id="3d6c9-130">Largeur de la zone englobante pour l’élément.</span><span class="sxs-lookup"><span data-stu-id="3d6c9-130">The width of the bounding box for the element.</span></span>                                          | <span data-ttu-id="3d6c9-131">Entier non négatif.</span><span class="sxs-lookup"><span data-stu-id="3d6c9-131">Any non-negative integer.</span></span> |
| <span data-ttu-id="3d6c9-132">**Height**</span><span class="sxs-lookup"><span data-stu-id="3d6c9-132">**Height**</span></span> | <span data-ttu-id="3d6c9-133">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="3d6c9-133">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="3d6c9-134">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="3d6c9-134">Required</span></span> | <span data-ttu-id="3d6c9-135">Hauteur du rectangle englobant pour l’élément.</span><span class="sxs-lookup"><span data-stu-id="3d6c9-135">The height of the bounding box for the element.</span></span>                                         | <span data-ttu-id="3d6c9-136">Entier non négatif.</span><span class="sxs-lookup"><span data-stu-id="3d6c9-136">Any non-negative integer.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="3d6c9-137">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="3d6c9-137">Element Information</span></span>



|              |                                                       |
|--------------|-------------------------------------------------------|
| <span data-ttu-id="3d6c9-138">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="3d6c9-138">Element type</span></span> | <span data-ttu-id="3d6c9-139">ComplexType [**FlagType**](flagtype-complex-type.md)</span><span class="sxs-lookup"><span data-stu-id="3d6c9-139">[**FlagType**](flagtype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="3d6c9-140">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="3d6c9-140">Namespace</span></span>    | <span data-ttu-id="3d6c9-141">urn : schemas-microsoft-com : TabletPC : RichInk</span><span class="sxs-lookup"><span data-stu-id="3d6c9-141">urn:schemas-microsoft-com:tabletpc:richink</span></span>            |
| <span data-ttu-id="3d6c9-142">Nom du schéma</span><span class="sxs-lookup"><span data-stu-id="3d6c9-142">Schema name</span></span>  | <span data-ttu-id="3d6c9-143">Lecteur de journal</span><span class="sxs-lookup"><span data-stu-id="3d6c9-143">Journal Reader</span></span>                                        |



 

 

 



