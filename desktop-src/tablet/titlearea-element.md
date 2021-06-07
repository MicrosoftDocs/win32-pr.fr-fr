---
description: Contient l’emplacement et les informations liées au titre de la note, le cas échéant.
ms.assetid: b193f6c2-5f26-41f9-acc8-d734c426b069
title: Élément partie titlearea
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88d563e8d7f6fc0107bc3302d3f8d94d29dfbfb8
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432191"
---
# <a name="titlearea-element"></a><span data-ttu-id="94bbb-103">Élément partie titlearea</span><span class="sxs-lookup"><span data-stu-id="94bbb-103">TitleArea Element</span></span>

<span data-ttu-id="94bbb-104">Contient l’emplacement et les informations liées au titre de la note, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="94bbb-104">Contains location and bounding information for the note Title, if present.</span></span>

## <a name="definition"></a><span data-ttu-id="94bbb-105">Définition</span><span class="sxs-lookup"><span data-stu-id="94bbb-105">Definition</span></span>

``` syntax
<xs:element name="TitleArea" type="TitleAreaType" minOccurs="0" />
```

## <a name="parent-elements"></a><span data-ttu-id="94bbb-106">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="94bbb-106">Parent Elements</span></span>

[<span data-ttu-id="94bbb-107">**Titre**</span><span class="sxs-lookup"><span data-stu-id="94bbb-107">**Title**</span></span>](title-element.md)

## <a name="child-elements"></a><span data-ttu-id="94bbb-108">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="94bbb-108">Child Elements</span></span>

<span data-ttu-id="94bbb-109">Aucun.</span><span class="sxs-lookup"><span data-stu-id="94bbb-109">None.</span></span>

## <a name="attributes"></a><span data-ttu-id="94bbb-110">Attributs</span><span class="sxs-lookup"><span data-stu-id="94bbb-110">Attributes</span></span>



| <span data-ttu-id="94bbb-111">Attribut</span><span class="sxs-lookup"><span data-stu-id="94bbb-111">Attribute</span></span>  | <span data-ttu-id="94bbb-112">Type</span><span class="sxs-lookup"><span data-stu-id="94bbb-112">Type</span></span>                      | <span data-ttu-id="94bbb-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="94bbb-113">Required</span></span> | <span data-ttu-id="94bbb-114">Description</span><span class="sxs-lookup"><span data-stu-id="94bbb-114">Description</span></span>                                                                             | <span data-ttu-id="94bbb-115">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="94bbb-115">Possible Values</span></span>           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| <span data-ttu-id="94bbb-116">**Left**</span><span class="sxs-lookup"><span data-stu-id="94bbb-116">**Left**</span></span>   | <span data-ttu-id="94bbb-117">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="94bbb-117">**xs:integer**</span></span>            | <span data-ttu-id="94bbb-118">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="94bbb-118">Required</span></span> | <span data-ttu-id="94bbb-119">Distance entre l’origine et le point le plus à gauche dans le cadre englobant de l’élément.</span><span class="sxs-lookup"><span data-stu-id="94bbb-119">The distance from the origin to the leftmost point in the bounding box for the element.</span></span> | <span data-ttu-id="94bbb-120">N’importe quel entier.</span><span class="sxs-lookup"><span data-stu-id="94bbb-120">Any integer.</span></span>              |
| <span data-ttu-id="94bbb-121">**Top**</span><span class="sxs-lookup"><span data-stu-id="94bbb-121">**Top**</span></span>    | <span data-ttu-id="94bbb-122">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="94bbb-122">**xs:integer**</span></span>            | <span data-ttu-id="94bbb-123">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="94bbb-123">Required</span></span> | <span data-ttu-id="94bbb-124">Distance entre l’origine et le point le plus élevé dans le cadre englobant de l’élément.</span><span class="sxs-lookup"><span data-stu-id="94bbb-124">The distance from the origin to the topmost point in the bounding box for the element.</span></span>  | <span data-ttu-id="94bbb-125">N’importe quel entier.</span><span class="sxs-lookup"><span data-stu-id="94bbb-125">Any integer.</span></span>              |
| <span data-ttu-id="94bbb-126">**Width**</span><span class="sxs-lookup"><span data-stu-id="94bbb-126">**Width**</span></span>  | <span data-ttu-id="94bbb-127">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="94bbb-127">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="94bbb-128">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="94bbb-128">Required</span></span> | <span data-ttu-id="94bbb-129">Largeur de la zone englobante pour l’élément.</span><span class="sxs-lookup"><span data-stu-id="94bbb-129">The width of the bounding box for the element.</span></span>                                          | <span data-ttu-id="94bbb-130">Entier non négatif.</span><span class="sxs-lookup"><span data-stu-id="94bbb-130">Any non-negative integer.</span></span> |
| <span data-ttu-id="94bbb-131">**Height**</span><span class="sxs-lookup"><span data-stu-id="94bbb-131">**Height**</span></span> | <span data-ttu-id="94bbb-132">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="94bbb-132">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="94bbb-133">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="94bbb-133">Required</span></span> | <span data-ttu-id="94bbb-134">Hauteur du rectangle englobant pour l’élément.</span><span class="sxs-lookup"><span data-stu-id="94bbb-134">The height of the bounding box for the element.</span></span>                                         | <span data-ttu-id="94bbb-135">Entier non négatif.</span><span class="sxs-lookup"><span data-stu-id="94bbb-135">Any non-negative integer.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="94bbb-136">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="94bbb-136">Element Information</span></span>



|   <span data-ttu-id="94bbb-137">Élément</span><span class="sxs-lookup"><span data-stu-id="94bbb-137">Element</span></span>    | <span data-ttu-id="94bbb-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="94bbb-138">Value</span></span>                                                           |
|--------------|-----------------------------------------------------------------|
| <span data-ttu-id="94bbb-139">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="94bbb-139">Element type</span></span> | <span data-ttu-id="94bbb-140">ComplexType [**TitleAreaType**](titleareatype-complex-type.md)</span><span class="sxs-lookup"><span data-stu-id="94bbb-140">[**TitleAreaType**](titleareatype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="94bbb-141">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="94bbb-141">Namespace</span></span>    | <span data-ttu-id="94bbb-142">urn : schemas-microsoft-com : TabletPC : RichInk</span><span class="sxs-lookup"><span data-stu-id="94bbb-142">urn:schemas-microsoft-com:tabletpc:richink</span></span>                      |
| <span data-ttu-id="94bbb-143">Nom du schéma</span><span class="sxs-lookup"><span data-stu-id="94bbb-143">Schema name</span></span>  | <span data-ttu-id="94bbb-144">Lecteur de journal</span><span class="sxs-lookup"><span data-stu-id="94bbb-144">Journal Reader</span></span>                                                  |



 

 

 



