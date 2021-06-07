---
description: Contient une bitmap encodée en base64 d’un indicateur associé à la section d’une note du journal.
ms.assetid: 612f8814-ab3c-4a3e-9791-525788d4cc72
title: Flag, élément
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46508f9821379fbedb3291ba45d16dbdd0fb316f
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432324"
---
# <a name="flag-element"></a><span data-ttu-id="f7090-103">Flag, élément</span><span class="sxs-lookup"><span data-stu-id="f7090-103">Flag Element</span></span>

<span data-ttu-id="f7090-104">Contient une bitmap encodée en base64 d’un indicateur associé à la section d’une note du journal.</span><span class="sxs-lookup"><span data-stu-id="f7090-104">Contains a base64 encoded bitmap of a flag associated with section of a Journal note.</span></span>

## <a name="definition"></a><span data-ttu-id="f7090-105">Définition</span><span class="sxs-lookup"><span data-stu-id="f7090-105">Definition</span></span>

``` syntax
<xs:element name="Flag" type="FlagType" minOccurs="0" maxOccurs="unbounded" />
```

## <a name="parent-elements"></a><span data-ttu-id="f7090-106">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="f7090-106">Parent Elements</span></span>

[<span data-ttu-id="f7090-107">**Humidité**</span><span class="sxs-lookup"><span data-stu-id="f7090-107">**Content**</span></span>](content-element--journal-reader.md)

[<span data-ttu-id="f7090-108">**, Nœud**</span><span class="sxs-lookup"><span data-stu-id="f7090-108">**GroupNode**</span></span>](groupnode-element.md)

## <a name="child-elements"></a><span data-ttu-id="f7090-109">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="f7090-109">Child Elements</span></span>

<span data-ttu-id="f7090-110">Aucun.</span><span class="sxs-lookup"><span data-stu-id="f7090-110">None.</span></span>

## <a name="attributes"></a><span data-ttu-id="f7090-111">Attributs</span><span class="sxs-lookup"><span data-stu-id="f7090-111">Attributes</span></span>



| <span data-ttu-id="f7090-112">Attribut</span><span class="sxs-lookup"><span data-stu-id="f7090-112">Attribute</span></span>  | <span data-ttu-id="f7090-113">Type</span><span class="sxs-lookup"><span data-stu-id="f7090-113">Type</span></span>                      | <span data-ttu-id="f7090-114">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="f7090-114">Required</span></span> | <span data-ttu-id="f7090-115">Description</span><span class="sxs-lookup"><span data-stu-id="f7090-115">Description</span></span>                                                                             | <span data-ttu-id="f7090-116">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="f7090-116">Possible Values</span></span>           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| <span data-ttu-id="f7090-117">**Left**</span><span class="sxs-lookup"><span data-stu-id="f7090-117">**Left**</span></span>   | <span data-ttu-id="f7090-118">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="f7090-118">**xs:integer**</span></span>            | <span data-ttu-id="f7090-119">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="f7090-119">Required</span></span> | <span data-ttu-id="f7090-120">Distance entre l’origine et le point le plus à gauche dans le cadre englobant de l’élément.</span><span class="sxs-lookup"><span data-stu-id="f7090-120">The distance from the origin to the leftmost point in the bounding box for the element.</span></span> | <span data-ttu-id="f7090-121">N’importe quel entier.</span><span class="sxs-lookup"><span data-stu-id="f7090-121">Any integer.</span></span>              |
| <span data-ttu-id="f7090-122">**Top**</span><span class="sxs-lookup"><span data-stu-id="f7090-122">**Top**</span></span>    | <span data-ttu-id="f7090-123">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="f7090-123">**xs:integer**</span></span>            | <span data-ttu-id="f7090-124">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="f7090-124">Required</span></span> | <span data-ttu-id="f7090-125">Distance entre l’origine et le point le plus élevé dans le cadre englobant de l’élément.</span><span class="sxs-lookup"><span data-stu-id="f7090-125">The distance from the origin to the topmost point in the bounding box for the element.</span></span>  | <span data-ttu-id="f7090-126">N’importe quel entier.</span><span class="sxs-lookup"><span data-stu-id="f7090-126">Any integer.</span></span>              |
| <span data-ttu-id="f7090-127">**Width**</span><span class="sxs-lookup"><span data-stu-id="f7090-127">**Width**</span></span>  | <span data-ttu-id="f7090-128">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="f7090-128">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="f7090-129">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="f7090-129">Required</span></span> | <span data-ttu-id="f7090-130">Largeur de la zone englobante pour l’élément.</span><span class="sxs-lookup"><span data-stu-id="f7090-130">The width of the bounding box for the element.</span></span>                                          | <span data-ttu-id="f7090-131">Entier non négatif.</span><span class="sxs-lookup"><span data-stu-id="f7090-131">Any non-negative integer.</span></span> |
| <span data-ttu-id="f7090-132">**Height**</span><span class="sxs-lookup"><span data-stu-id="f7090-132">**Height**</span></span> | <span data-ttu-id="f7090-133">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="f7090-133">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="f7090-134">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="f7090-134">Required</span></span> | <span data-ttu-id="f7090-135">Hauteur du rectangle englobant pour l’élément.</span><span class="sxs-lookup"><span data-stu-id="f7090-135">The height of the bounding box for the element.</span></span>                                         | <span data-ttu-id="f7090-136">Entier non négatif.</span><span class="sxs-lookup"><span data-stu-id="f7090-136">Any non-negative integer.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="f7090-137">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="f7090-137">Element Information</span></span>



|  <span data-ttu-id="f7090-138">Élément</span><span class="sxs-lookup"><span data-stu-id="f7090-138">Element</span></span>     | <span data-ttu-id="f7090-139">Valeur</span><span class="sxs-lookup"><span data-stu-id="f7090-139">Value</span></span>                                                     |
|--------------|-------------------------------------------------------|
| <span data-ttu-id="f7090-140">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="f7090-140">Element type</span></span> | <span data-ttu-id="f7090-141">ComplexType [**FlagType**](flagtype-complex-type.md)</span><span class="sxs-lookup"><span data-stu-id="f7090-141">[**FlagType**](flagtype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="f7090-142">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="f7090-142">Namespace</span></span>    | <span data-ttu-id="f7090-143">urn : schemas-microsoft-com : TabletPC : RichInk</span><span class="sxs-lookup"><span data-stu-id="f7090-143">urn:schemas-microsoft-com:tabletpc:richink</span></span>            |
| <span data-ttu-id="f7090-144">Nom du schéma</span><span class="sxs-lookup"><span data-stu-id="f7090-144">Schema name</span></span>  | <span data-ttu-id="f7090-145">Lecteur de journal</span><span class="sxs-lookup"><span data-stu-id="f7090-145">Journal Reader</span></span>                                        |



 

 

 



