---
description: Contient les informations textuelles de la note du journal.
ms.assetid: 09ec2e8a-bd50-4f82-8ce3-a1c61f48ddb7
title: Text, élément
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 570f613a06f9fe814bfb1acbdbdba040dbc1119f
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432315"
---
# <a name="text-element"></a><span data-ttu-id="c63dd-103">Text, élément</span><span class="sxs-lookup"><span data-stu-id="c63dd-103">Text Element</span></span>

<span data-ttu-id="c63dd-104">Contient les informations textuelles de la note du journal.</span><span class="sxs-lookup"><span data-stu-id="c63dd-104">Contains text information from the Journal note.</span></span>

## <a name="definition"></a><span data-ttu-id="c63dd-105">Définition</span><span class="sxs-lookup"><span data-stu-id="c63dd-105">Definition</span></span>

<span data-ttu-id="c63dd-106">En cas d’utilisation avec le [**contenu**](content-element--journal-reader.md):</span><span class="sxs-lookup"><span data-stu-id="c63dd-106">When used with [**Content**](content-element--journal-reader.md):</span></span>

``` syntax
<xs:element name="Text" type="TextType" />
```

<span data-ttu-id="c63dd-107">Ou, en cas d’utilisation avec [**TitleInfo**](titleinfo-element.md) et [**, nœud**](groupnode-element.md):</span><span class="sxs-lookup"><span data-stu-id="c63dd-107">Or, when used with [**TitleInfo**](titleinfo-element.md) and [**GroupNode**](groupnode-element.md):</span></span>

``` syntax
<xs:element name="Text" type="xs:string" />
```

## <a name="parent-elements"></a><span data-ttu-id="c63dd-108">Éléments parents</span><span class="sxs-lookup"><span data-stu-id="c63dd-108">Parent Elements</span></span>

[<span data-ttu-id="c63dd-109">**Humidité**</span><span class="sxs-lookup"><span data-stu-id="c63dd-109">**Content**</span></span>](content-element--journal-reader.md)

[<span data-ttu-id="c63dd-110">**, Nœud**</span><span class="sxs-lookup"><span data-stu-id="c63dd-110">**GroupNode**</span></span>](groupnode-element.md)

[<span data-ttu-id="c63dd-111">**TitleInfo**</span><span class="sxs-lookup"><span data-stu-id="c63dd-111">**TitleInfo**</span></span>](titleinfo-element.md)

## <a name="child-elements"></a><span data-ttu-id="c63dd-112">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="c63dd-112">Child Elements</span></span>

<span data-ttu-id="c63dd-113">Aucun.</span><span class="sxs-lookup"><span data-stu-id="c63dd-113">None.</span></span>

## <a name="attributes"></a><span data-ttu-id="c63dd-114">Attributs</span><span class="sxs-lookup"><span data-stu-id="c63dd-114">Attributes</span></span>

<span data-ttu-id="c63dd-115">Il n’existe aucun attribut lorsqu’il est utilisé avec [**TitleInfo**](titleinfo-element.md) et [**, nœud**](groupnode-element.md).</span><span class="sxs-lookup"><span data-stu-id="c63dd-115">There are no attributes when used with [**TitleInfo**](titleinfo-element.md) and [**GroupNode**](groupnode-element.md).</span></span> <span data-ttu-id="c63dd-116">Lorsqu’ils sont utilisés avec du [**contenu**](content-element--journal-reader.md), les attributs sont les suivants.</span><span class="sxs-lookup"><span data-stu-id="c63dd-116">When used with [**Content**](content-element--journal-reader.md), the attributes are as follows.</span></span>



| <span data-ttu-id="c63dd-117">Attribut</span><span class="sxs-lookup"><span data-stu-id="c63dd-117">Attribute</span></span>  | <span data-ttu-id="c63dd-118">Type</span><span class="sxs-lookup"><span data-stu-id="c63dd-118">Type</span></span>                      | <span data-ttu-id="c63dd-119">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="c63dd-119">Required</span></span> | <span data-ttu-id="c63dd-120">Description</span><span class="sxs-lookup"><span data-stu-id="c63dd-120">Description</span></span>                                                                             | <span data-ttu-id="c63dd-121">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="c63dd-121">Possible Values</span></span>           |
|------------|---------------------------|----------|-----------------------------------------------------------------------------------------|---------------------------|
| <span data-ttu-id="c63dd-122">**Left**</span><span class="sxs-lookup"><span data-stu-id="c63dd-122">**Left**</span></span>   | <span data-ttu-id="c63dd-123">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="c63dd-123">**xs:integer**</span></span>            | <span data-ttu-id="c63dd-124">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="c63dd-124">Required</span></span> | <span data-ttu-id="c63dd-125">Distance entre l’origine et le point le plus à gauche dans le cadre englobant de l’élément.</span><span class="sxs-lookup"><span data-stu-id="c63dd-125">The distance from the origin to the leftmost point in the bounding box for the element.</span></span> | <span data-ttu-id="c63dd-126">N’importe quel entier.</span><span class="sxs-lookup"><span data-stu-id="c63dd-126">Any integer.</span></span>              |
| <span data-ttu-id="c63dd-127">**Top**</span><span class="sxs-lookup"><span data-stu-id="c63dd-127">**Top**</span></span>    | <span data-ttu-id="c63dd-128">**xs:integer**</span><span class="sxs-lookup"><span data-stu-id="c63dd-128">**xs:integer**</span></span>            | <span data-ttu-id="c63dd-129">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="c63dd-129">Required</span></span> | <span data-ttu-id="c63dd-130">Distance entre l’origine et le point le plus élevé dans le cadre englobant de l’élément.</span><span class="sxs-lookup"><span data-stu-id="c63dd-130">The distance from the origin to the topmost point in the bounding box for the element.</span></span>  | <span data-ttu-id="c63dd-131">N’importe quel entier.</span><span class="sxs-lookup"><span data-stu-id="c63dd-131">Any integer.</span></span>              |
| <span data-ttu-id="c63dd-132">**Width**</span><span class="sxs-lookup"><span data-stu-id="c63dd-132">**Width**</span></span>  | <span data-ttu-id="c63dd-133">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="c63dd-133">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="c63dd-134">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="c63dd-134">Required</span></span> | <span data-ttu-id="c63dd-135">Largeur de la zone englobante pour l’élément.</span><span class="sxs-lookup"><span data-stu-id="c63dd-135">The width of the bounding box for the element.</span></span>                                          | <span data-ttu-id="c63dd-136">Entier non négatif.</span><span class="sxs-lookup"><span data-stu-id="c63dd-136">Any non-negative integer.</span></span> |
| <span data-ttu-id="c63dd-137">**Height**</span><span class="sxs-lookup"><span data-stu-id="c63dd-137">**Height**</span></span> | <span data-ttu-id="c63dd-138">**xs:nonNegativeInteger**</span><span class="sxs-lookup"><span data-stu-id="c63dd-138">**xs:nonNegativeInteger**</span></span> | <span data-ttu-id="c63dd-139">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="c63dd-139">Required</span></span> | <span data-ttu-id="c63dd-140">Hauteur du rectangle englobant pour l’élément.</span><span class="sxs-lookup"><span data-stu-id="c63dd-140">The height of the bounding box for the element.</span></span>                                         | <span data-ttu-id="c63dd-141">Entier non négatif.</span><span class="sxs-lookup"><span data-stu-id="c63dd-141">Any non-negative integer.</span></span> |



 

## <a name="element-information"></a><span data-ttu-id="c63dd-142">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="c63dd-142">Element Information</span></span>



|   <span data-ttu-id="c63dd-143">Élément</span><span class="sxs-lookup"><span data-stu-id="c63dd-143">Element</span></span>           |   <span data-ttu-id="c63dd-144">Valeur</span><span class="sxs-lookup"><span data-stu-id="c63dd-144">Value</span></span>                                |
|--------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c63dd-145">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="c63dd-145">Element type</span></span> | <span data-ttu-id="c63dd-146">[**TextType**](texttype-complex-type.md) complexType (avec l’élément content) ou **XS : String** (avec les éléments [**, nœud**](groupnode-element.md) et [**TitleInfo**](titleinfo-element.md) )</span><span class="sxs-lookup"><span data-stu-id="c63dd-146">[**TextType**](texttype-complex-type.md) complexType (with the Content element) or **xs:string** (with [**GroupNode**](groupnode-element.md) and [**TitleInfo**](titleinfo-element.md) elements)</span></span> |
| <span data-ttu-id="c63dd-147">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="c63dd-147">Namespace</span></span>    | <span data-ttu-id="c63dd-148">urn : schemas-microsoft-com : TabletPC : RichInk</span><span class="sxs-lookup"><span data-stu-id="c63dd-148">urn:schemas-microsoft-com:tabletpc:richink</span></span><br/>                                                                                                                                               |
| <span data-ttu-id="c63dd-149">Nom du schéma</span><span class="sxs-lookup"><span data-stu-id="c63dd-149">Schema name</span></span>  | <span data-ttu-id="c63dd-150">Lecteur de journal</span><span class="sxs-lookup"><span data-stu-id="c63dd-150">Journal Reader</span></span><br/>                                                                                                                                                                           |



 

 

 




