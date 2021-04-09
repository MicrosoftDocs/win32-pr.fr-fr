---
description: Contient les informations textuelles de la note du journal.
ms.assetid: 09ec2e8a-bd50-4f82-8ce3-a1c61f48ddb7
title: Text, élément
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed9c72fe584d0e796d4a6f897297aa60bbeddc5d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952912"
---
# <a name="text-element"></a><span data-ttu-id="4264c-103">Text, élément</span><span class="sxs-lookup"><span data-stu-id="4264c-103">Text Element</span></span>

<span data-ttu-id="4264c-104">Contient les informations textuelles de la note du journal.</span><span class="sxs-lookup"><span data-stu-id="4264c-104">Contains text information from the Journal note.</span></span>

## <a name="definition"></a><span data-ttu-id="4264c-105">Définition</span><span class="sxs-lookup"><span data-stu-id="4264c-105">Definition</span></span>

<span data-ttu-id="4264c-106">En cas d’utilisation avec le [**contenu**](content-element--journal-reader.md):</span><span class="sxs-lookup"><span data-stu-id="4264c-106">When used with [**Content**](content-element--journal-reader.md):</span></span>

``` syntax
<xs:element name="Text" type="TextType" />
```

<span data-ttu-id="4264c-107">Ou, en cas d’utilisation avec [**TitleInfo**](titleinfo-element.md) et [**, nœud**](groupnode-element.md):</span><span class="sxs-lookup"><span data-stu-id="4264c-107">Or, when used with [**TitleInfo**](titleinfo-element.md) and [**GroupNode**](groupnode-element.md):</span></span>

``` syntax
<xs:element name="Text" type="xs:string" />
```

## <a name="parent-elements"></a><span data-ttu-id="4264c-108">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="4264c-108">Parent Elements</span></span>

[<span data-ttu-id="4264c-109">**Content**</span><span class="sxs-lookup"><span data-stu-id="4264c-109">**Content**</span></span>](content-element--journal-reader.md)

[<span data-ttu-id="4264c-110">**, Nœud**</span><span class="sxs-lookup"><span data-stu-id="4264c-110">**GroupNode**</span></span>](groupnode-element.md)

[<span data-ttu-id="4264c-111">**TitleInfo**</span><span class="sxs-lookup"><span data-stu-id="4264c-111">**TitleInfo**</span></span>](titleinfo-element.md)

## <a name="child-elements"></a><span data-ttu-id="4264c-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="4264c-112">Child Elements</span></span>

<span data-ttu-id="4264c-113">Aucun</span><span class="sxs-lookup"><span data-stu-id="4264c-113">None.</span></span>

## <a name="attributes"></a><span data-ttu-id="4264c-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="4264c-114">Attributes</span></span>

<span data-ttu-id="4264c-115">Il n’existe aucun attribut lorsqu’il est utilisé avec [**TitleInfo**](titleinfo-element.md) et [**, nœud**](groupnode-element.md).</span><span class="sxs-lookup"><span data-stu-id="4264c-115">There are no attributes when used with [**TitleInfo**](titleinfo-element.md) and [**GroupNode**](groupnode-element.md).</span></span> <span data-ttu-id="4264c-116">Lorsqu’ils sont utilisés avec du [**contenu**](content-element--journal-reader.md), les attributs sont les suivants.</span><span class="sxs-lookup"><span data-stu-id="4264c-116">When used with [**Content**](content-element--journal-reader.md), the attributes are as follows.</span></span>



| <span data-ttu-id="4264c-117">Attribut</span><span class="sxs-lookup"><span data-stu-id="4264c-117">Attribute</span></span>  | <span data-ttu-id="4264c-118">Type</span><span class="sxs-lookup"><span data-stu-id="4264c-118">Type</span></span>                      | <span data-ttu-id="4264c-119">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="4264c-119">Required</span></span> | <span data-ttu-id="4264c-120">Description</span><span class="sxs-lookup"><span data-stu-id="4264c-120">Description</span></span>                                                                             | <span data-ttu-id="4264c-121">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="4264c-121">Possible Values</span></span>           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| <span data-ttu-id="4264c-122">**Left**</span><span class="sxs-lookup"><span data-stu-id="4264c-122">**Left**</span></span>   | <span data-ttu-id="4264c-123">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="4264c-123">**xs:integer**</span></span>            | <span data-ttu-id="4264c-124">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="4264c-124">Required</span></span> | <span data-ttu-id="4264c-125">Distance entre l’origine et le point le plus à gauche dans le cadre englobant de l’élément.</span><span class="sxs-lookup"><span data-stu-id="4264c-125">The distance from the origin to the leftmost point in the bounding box for the element.</span></span> | <span data-ttu-id="4264c-126">N’importe quel entier.</span><span class="sxs-lookup"><span data-stu-id="4264c-126">Any integer.</span></span>              |
| <span data-ttu-id="4264c-127">**Top**</span><span class="sxs-lookup"><span data-stu-id="4264c-127">**Top**</span></span>    | <span data-ttu-id="4264c-128">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="4264c-128">**xs:integer**</span></span>            | <span data-ttu-id="4264c-129">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="4264c-129">Required</span></span> | <span data-ttu-id="4264c-130">Distance entre l’origine et le point le plus élevé dans le cadre englobant de l’élément.</span><span class="sxs-lookup"><span data-stu-id="4264c-130">The distance from the origin to the topmost point in the bounding box for the element.</span></span>  | <span data-ttu-id="4264c-131">N’importe quel entier.</span><span class="sxs-lookup"><span data-stu-id="4264c-131">Any integer.</span></span>              |
| <span data-ttu-id="4264c-132">**Width**</span><span class="sxs-lookup"><span data-stu-id="4264c-132">**Width**</span></span>  | <span data-ttu-id="4264c-133">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="4264c-133">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="4264c-134">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="4264c-134">Required</span></span> | <span data-ttu-id="4264c-135">Largeur de la zone englobante pour l’élément.</span><span class="sxs-lookup"><span data-stu-id="4264c-135">The width of the bounding box for the element.</span></span>                                          | <span data-ttu-id="4264c-136">Entier non négatif.</span><span class="sxs-lookup"><span data-stu-id="4264c-136">Any non-negative integer.</span></span> |
| <span data-ttu-id="4264c-137">**Height**</span><span class="sxs-lookup"><span data-stu-id="4264c-137">**Height**</span></span> | <span data-ttu-id="4264c-138">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="4264c-138">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="4264c-139">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="4264c-139">Required</span></span> | <span data-ttu-id="4264c-140">Hauteur du rectangle englobant pour l’élément.</span><span class="sxs-lookup"><span data-stu-id="4264c-140">The height of the bounding box for the element.</span></span>                                         | <span data-ttu-id="4264c-141">Entier non négatif.</span><span class="sxs-lookup"><span data-stu-id="4264c-141">Any non-negative integer.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="4264c-142">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="4264c-142">Element Information</span></span>



|              |                                                                                                                                                                                                     |
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4264c-143">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="4264c-143">Element type</span></span> | <span data-ttu-id="4264c-144">[**TextType**](texttype-complex-type.md) complexType (avec l’élément content) ou **XS : String** (avec les éléments [**, nœud**](groupnode-element.md) et [**TitleInfo**](titleinfo-element.md) )</span><span class="sxs-lookup"><span data-stu-id="4264c-144">[**TextType**](texttype-complex-type.md) complexType (with the Content element) or **xs:string** (with [**GroupNode**](groupnode-element.md) and [**TitleInfo**](titleinfo-element.md) elements)</span></span> |
| <span data-ttu-id="4264c-145">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="4264c-145">Namespace</span></span>    | <span data-ttu-id="4264c-146">urn : schemas-microsoft-com : TabletPC : RichInk</span><span class="sxs-lookup"><span data-stu-id="4264c-146">urn:schemas-microsoft-com:tabletpc:richink</span></span><br/>                                                                                                                                               |
| <span data-ttu-id="4264c-147">Nom du schéma</span><span class="sxs-lookup"><span data-stu-id="4264c-147">Schema name</span></span>  | <span data-ttu-id="4264c-148">Lecteur de journal</span><span class="sxs-lookup"><span data-stu-id="4264c-148">Journal Reader</span></span><br/>                                                                                                                                                                           |



 

 

 




