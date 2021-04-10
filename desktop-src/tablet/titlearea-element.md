---
description: Contient l’emplacement et les informations liées au titre de la note, le cas échéant.
ms.assetid: b193f6c2-5f26-41f9-acc8-d734c426b069
title: Élément partie titlearea
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c009d817af9679edda618dd0262c7cbb85a612ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103953011"
---
# <a name="titlearea-element"></a><span data-ttu-id="66924-103">Élément partie titlearea</span><span class="sxs-lookup"><span data-stu-id="66924-103">TitleArea Element</span></span>

<span data-ttu-id="66924-104">Contient l’emplacement et les informations liées au titre de la note, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="66924-104">Contains location and bounding information for the note Title, if present.</span></span>

## <a name="definition"></a><span data-ttu-id="66924-105">Définition</span><span class="sxs-lookup"><span data-stu-id="66924-105">Definition</span></span>

``` syntax
<xs:element name="TitleArea" type="TitleAreaType" minOccurs="0" />
```

## <a name="parent-elements"></a><span data-ttu-id="66924-106">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="66924-106">Parent Elements</span></span>

[<span data-ttu-id="66924-107">**Intitulé**</span><span class="sxs-lookup"><span data-stu-id="66924-107">**Title**</span></span>](title-element.md)

## <a name="child-elements"></a><span data-ttu-id="66924-108">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="66924-108">Child Elements</span></span>

<span data-ttu-id="66924-109">Aucun</span><span class="sxs-lookup"><span data-stu-id="66924-109">None.</span></span>

## <a name="attributes"></a><span data-ttu-id="66924-110">Attributs</span><span class="sxs-lookup"><span data-stu-id="66924-110">Attributes</span></span>



| <span data-ttu-id="66924-111">Attribut</span><span class="sxs-lookup"><span data-stu-id="66924-111">Attribute</span></span>  | <span data-ttu-id="66924-112">Type</span><span class="sxs-lookup"><span data-stu-id="66924-112">Type</span></span>                      | <span data-ttu-id="66924-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="66924-113">Required</span></span> | <span data-ttu-id="66924-114">Description</span><span class="sxs-lookup"><span data-stu-id="66924-114">Description</span></span>                                                                             | <span data-ttu-id="66924-115">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="66924-115">Possible Values</span></span>           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| <span data-ttu-id="66924-116">**Left**</span><span class="sxs-lookup"><span data-stu-id="66924-116">**Left**</span></span>   | <span data-ttu-id="66924-117">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="66924-117">**xs:integer**</span></span>            | <span data-ttu-id="66924-118">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="66924-118">Required</span></span> | <span data-ttu-id="66924-119">Distance entre l’origine et le point le plus à gauche dans le cadre englobant de l’élément.</span><span class="sxs-lookup"><span data-stu-id="66924-119">The distance from the origin to the leftmost point in the bounding box for the element.</span></span> | <span data-ttu-id="66924-120">N’importe quel entier.</span><span class="sxs-lookup"><span data-stu-id="66924-120">Any integer.</span></span>              |
| <span data-ttu-id="66924-121">**Top**</span><span class="sxs-lookup"><span data-stu-id="66924-121">**Top**</span></span>    | <span data-ttu-id="66924-122">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="66924-122">**xs:integer**</span></span>            | <span data-ttu-id="66924-123">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="66924-123">Required</span></span> | <span data-ttu-id="66924-124">Distance entre l’origine et le point le plus élevé dans le cadre englobant de l’élément.</span><span class="sxs-lookup"><span data-stu-id="66924-124">The distance from the origin to the topmost point in the bounding box for the element.</span></span>  | <span data-ttu-id="66924-125">N’importe quel entier.</span><span class="sxs-lookup"><span data-stu-id="66924-125">Any integer.</span></span>              |
| <span data-ttu-id="66924-126">**Width**</span><span class="sxs-lookup"><span data-stu-id="66924-126">**Width**</span></span>  | <span data-ttu-id="66924-127">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="66924-127">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="66924-128">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="66924-128">Required</span></span> | <span data-ttu-id="66924-129">Largeur de la zone englobante pour l’élément.</span><span class="sxs-lookup"><span data-stu-id="66924-129">The width of the bounding box for the element.</span></span>                                          | <span data-ttu-id="66924-130">Entier non négatif.</span><span class="sxs-lookup"><span data-stu-id="66924-130">Any non-negative integer.</span></span> |
| <span data-ttu-id="66924-131">**Height**</span><span class="sxs-lookup"><span data-stu-id="66924-131">**Height**</span></span> | <span data-ttu-id="66924-132">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="66924-132">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="66924-133">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="66924-133">Required</span></span> | <span data-ttu-id="66924-134">Hauteur du rectangle englobant pour l’élément.</span><span class="sxs-lookup"><span data-stu-id="66924-134">The height of the bounding box for the element.</span></span>                                         | <span data-ttu-id="66924-135">Entier non négatif.</span><span class="sxs-lookup"><span data-stu-id="66924-135">Any non-negative integer.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="66924-136">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="66924-136">Element Information</span></span>



|              |                                                                 |
|--------------|-----------------------------------------------------------------|
| <span data-ttu-id="66924-137">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="66924-137">Element type</span></span> | <span data-ttu-id="66924-138">ComplexType [**TitleAreaType**](titleareatype-complex-type.md)</span><span class="sxs-lookup"><span data-stu-id="66924-138">[**TitleAreaType**](titleareatype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="66924-139">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="66924-139">Namespace</span></span>    | <span data-ttu-id="66924-140">urn : schemas-microsoft-com : TabletPC : RichInk</span><span class="sxs-lookup"><span data-stu-id="66924-140">urn:schemas-microsoft-com:tabletpc:richink</span></span>                      |
| <span data-ttu-id="66924-141">Nom du schéma</span><span class="sxs-lookup"><span data-stu-id="66924-141">Schema name</span></span>  | <span data-ttu-id="66924-142">Lecteur de journal</span><span class="sxs-lookup"><span data-stu-id="66924-142">Journal Reader</span></span>                                                  |



 

 

 



