---
description: Définit un groupe d’attributs utilisé par divers éléments dans un fichier journal XML. Elle contient des attributs utilisés pour définir les limites (gauche, haut, hauteur et largeur) d’un élément dans le document.
ms.assetid: 7841aa65-fb35-4909-a34e-3c883555f764
title: Groupe d’attributs BoundsType
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 411a9d3ec30363e5c405cf27654330a0886f8946
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749108"
---
# <a name="boundstype-attribute-group"></a><span data-ttu-id="49fce-104">Groupe d’attributs BoundsType</span><span class="sxs-lookup"><span data-stu-id="49fce-104">BoundsType Attribute Group</span></span>

<span data-ttu-id="49fce-105">Définit un groupe d’attributs utilisé par divers éléments dans un fichier journal XML.</span><span class="sxs-lookup"><span data-stu-id="49fce-105">Defines an attribute group that is used by a variety of elements in a Journal XML file.</span></span> <span data-ttu-id="49fce-106">Elle contient des attributs utilisés pour définir les limites (gauche, haut, hauteur et largeur) d’un élément dans le document.</span><span class="sxs-lookup"><span data-stu-id="49fce-106">It contains attributes used to define the bounds (left, top, height, and width) of an element in the document.</span></span>

## <a name="definition"></a><span data-ttu-id="49fce-107">Définition</span><span class="sxs-lookup"><span data-stu-id="49fce-107">Definition</span></span>

``` syntax
<xs:attributeGroup name="BoundsType">
  <xs:attribute name="Left" use="required" type="xs:integer" />
  <xs:attribute name="Top" use="required" type="xs:integer" />
  <xs:attribute name="Width" use="required" type="xs:nonNegativeInteger" />
  <xs:attribute name="Height" use="required" type="xs: nonNegativeInteger" />
</xs:attributeGroup>
```

## <a name="child-elements"></a><span data-ttu-id="49fce-108">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="49fce-108">Child Elements</span></span>

<span data-ttu-id="49fce-109">Aucun</span><span class="sxs-lookup"><span data-stu-id="49fce-109">None.</span></span>

## <a name="attributes"></a><span data-ttu-id="49fce-110">Attributs</span><span class="sxs-lookup"><span data-stu-id="49fce-110">Attributes</span></span>



| <span data-ttu-id="49fce-111">Attribut</span><span class="sxs-lookup"><span data-stu-id="49fce-111">Attribute</span></span>  | <span data-ttu-id="49fce-112">Type</span><span class="sxs-lookup"><span data-stu-id="49fce-112">Type</span></span>                      | <span data-ttu-id="49fce-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="49fce-113">Required</span></span> | <span data-ttu-id="49fce-114">Description</span><span class="sxs-lookup"><span data-stu-id="49fce-114">Description</span></span>                                                                                        | <span data-ttu-id="49fce-115">PossibleValues</span><span class="sxs-lookup"><span data-stu-id="49fce-115">PossibleValues</span></span>                       |
|------------|---------------------------|----------|----------------------------------------------------------------------------------------------------|--------------------------------------|
| <span data-ttu-id="49fce-116">**Left**</span><span class="sxs-lookup"><span data-stu-id="49fce-116">**Left**</span></span>   | <span data-ttu-id="49fce-117">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="49fce-117">**xs:integer**</span></span>            | <span data-ttu-id="49fce-118">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="49fce-118">Required</span></span> | <span data-ttu-id="49fce-119">Distance entre l’origine et le point le plus à gauche dans le cadre englobant de l’élément.</span><span class="sxs-lookup"><span data-stu-id="49fce-119">The distance from the origin to the leftmost point in the bounding box for the element.</span></span><br/> | <span data-ttu-id="49fce-120">N’importe quel entier.</span><span class="sxs-lookup"><span data-stu-id="49fce-120">Any integer.</span></span><br/>              |
| <span data-ttu-id="49fce-121">**Top**</span><span class="sxs-lookup"><span data-stu-id="49fce-121">**Top**</span></span>    | <span data-ttu-id="49fce-122">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="49fce-122">**xs:integer**</span></span>            | <span data-ttu-id="49fce-123">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="49fce-123">Required</span></span> | <span data-ttu-id="49fce-124">Distance entre l’origine et le point le plus élevé dans le cadre englobant de l’élément.</span><span class="sxs-lookup"><span data-stu-id="49fce-124">The distance from the origin to the topmost point in the bounding box for the element.</span></span><br/>  | <span data-ttu-id="49fce-125">N’importe quel entier.</span><span class="sxs-lookup"><span data-stu-id="49fce-125">Any integer.</span></span><br/>              |
| <span data-ttu-id="49fce-126">**Width**</span><span class="sxs-lookup"><span data-stu-id="49fce-126">**Width**</span></span>  | <span data-ttu-id="49fce-127">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="49fce-127">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="49fce-128">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="49fce-128">Required</span></span> | <span data-ttu-id="49fce-129">Largeur de la zone englobante pour l’élément.</span><span class="sxs-lookup"><span data-stu-id="49fce-129">The width of the bounding box for the element.</span></span><br/>                                          | <span data-ttu-id="49fce-130">Entier non négatif.</span><span class="sxs-lookup"><span data-stu-id="49fce-130">Any non-negative integer.</span></span><br/> |
| <span data-ttu-id="49fce-131">**Height**</span><span class="sxs-lookup"><span data-stu-id="49fce-131">**Height**</span></span> | <span data-ttu-id="49fce-132">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="49fce-132">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="49fce-133">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="49fce-133">Required</span></span> | <span data-ttu-id="49fce-134">Hauteur du rectangle englobant pour l’élément.</span><span class="sxs-lookup"><span data-stu-id="49fce-134">The height of the bounding box for the element.</span></span><br/>                                         | <span data-ttu-id="49fce-135">Entier non négatif.</span><span class="sxs-lookup"><span data-stu-id="49fce-135">Any non-negative integer.</span></span><br/> |



 

## <a name="type-information"></a><span data-ttu-id="49fce-136">Informations de type</span><span class="sxs-lookup"><span data-stu-id="49fce-136">Type Information</span></span>



|             |                                            |
|-------------|--------------------------------------------|
| <span data-ttu-id="49fce-137">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="49fce-137">Namespace</span></span>   | <span data-ttu-id="49fce-138">urn : schemas-microsoft-com : TabletPC : RichInk</span><span class="sxs-lookup"><span data-stu-id="49fce-138">urn:schemas-microsoft-com:tabletpc:richink</span></span> |
| <span data-ttu-id="49fce-139">Nom du schéma</span><span class="sxs-lookup"><span data-stu-id="49fce-139">Schema name</span></span> | <span data-ttu-id="49fce-140">Lecteur de journal</span><span class="sxs-lookup"><span data-stu-id="49fce-140">Journal Reader</span></span>                             |



 

## <a name="remarks"></a><span data-ttu-id="49fce-141">Notes</span><span class="sxs-lookup"><span data-stu-id="49fce-141">Remarks</span></span>

<span data-ttu-id="49fce-142">**Left** et **Top** peuvent être négatifs, car l’origine est définie par les marges, et non par la page.</span><span class="sxs-lookup"><span data-stu-id="49fce-142">**Left** and **Top** can be negative because the origin is defined by the margins, not the page.</span></span>

 

 




