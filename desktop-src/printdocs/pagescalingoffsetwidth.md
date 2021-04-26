---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: e82394d1-f765-4679-b1de-ea17825d6478
title: PageScalingOffsetWidth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b82c2b0c0f2c86a792706ec7e00819ccda1038c
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997956"
---
# <a name="pagescalingoffsetwidth"></a><span data-ttu-id="083d9-104">PageScalingOffsetWidth</span><span class="sxs-lookup"><span data-stu-id="083d9-104">PageScalingOffsetWidth</span></span>

<span data-ttu-id="083d9-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="083d9-105">This topic is not current.</span></span> <span data-ttu-id="083d9-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="083d9-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="083d9-107">Spécifie le décalage de mise à l’échelle dans la direction ImageableSizeWidth pour la mise à l’échelle personnalisée.</span><span class="sxs-lookup"><span data-stu-id="083d9-107">Specifies the scaling offset in the ImageableSizeWidth direction for custom scaling.</span></span>

-   [<span data-ttu-id="083d9-108">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="083d9-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="083d9-109">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="083d9-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="083d9-110">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="083d9-110">Element Information</span></span>



| <span data-ttu-id="083d9-111">Nom</span><span class="sxs-lookup"><span data-stu-id="083d9-111">Name</span></span> | <span data-ttu-id="083d9-112">Value</span><span class="sxs-lookup"><span data-stu-id="083d9-112">Value</span></span> |
|----------------------------|---------------------------------------------------------|
| <span data-ttu-id="083d9-113">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="083d9-113">Element Type</span></span> <br/>   | <span data-ttu-id="083d9-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="083d9-114">ParameterDef</span></span><br/>                                 |
| <span data-ttu-id="083d9-115">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="083d9-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="083d9-116">Page</span><span class="sxs-lookup"><span data-stu-id="083d9-116">Page</span></span><br/>                                         |
| <span data-ttu-id="083d9-117">Notes</span><span class="sxs-lookup"><span data-stu-id="083d9-117">Notes</span></span> <br/>          | <span data-ttu-id="083d9-118">Lié à l’élément PageScaling, option personnalisée</span><span class="sxs-lookup"><span data-stu-id="083d9-118">Linked to PageScaling element, Custom option</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="083d9-119">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="083d9-119">Structure Content</span></span>

<span data-ttu-id="083d9-120">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="083d9-120">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageScalingOffsetWidth">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:integer</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxValue">
    <psf:Value xsi:type="xs:integer">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinValue">
    <psf:Value xsi:type="xs:decimal">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Multiple">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Conditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">microns</psf:Value>
  </psf:Property>
</psf:ParameterDef>
      
```

## <a name="structure-properties"></a><span data-ttu-id="083d9-121">Propriétés de structure</span><span class="sxs-lookup"><span data-stu-id="083d9-121">Structure Properties</span></span>

<span data-ttu-id="083d9-122">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="083d9-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="083d9-123">Propriété</span><span class="sxs-lookup"><span data-stu-id="083d9-123">Property</span></span>                | <span data-ttu-id="083d9-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="083d9-124">xsi:type</span></span>           | <span data-ttu-id="083d9-125">Value</span><span class="sxs-lookup"><span data-stu-id="083d9-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="083d9-126">DataType</span><span class="sxs-lookup"><span data-stu-id="083d9-126">DataType</span></span><br/>     | <span data-ttu-id="083d9-127">string</span><span class="sxs-lookup"><span data-stu-id="083d9-127">string</span></span><br/>  | <span data-ttu-id="083d9-128">xs:integer</span><span class="sxs-lookup"><span data-stu-id="083d9-128">xs:integer</span></span><br/>      |
| <span data-ttu-id="083d9-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="083d9-129">DefaultValue</span></span><br/> | <span data-ttu-id="083d9-130">entier</span><span class="sxs-lookup"><span data-stu-id="083d9-130">integer</span></span><br/> | <span data-ttu-id="083d9-131">non défini</span><span class="sxs-lookup"><span data-stu-id="083d9-131">undefined</span></span><br/>       |
| <span data-ttu-id="083d9-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="083d9-132">MaxValue</span></span><br/>     | <span data-ttu-id="083d9-133">entier</span><span class="sxs-lookup"><span data-stu-id="083d9-133">integer</span></span><br/> | <span data-ttu-id="083d9-134">non défini</span><span class="sxs-lookup"><span data-stu-id="083d9-134">undefined</span></span><br/>       |
| <span data-ttu-id="083d9-135">MinValue</span><span class="sxs-lookup"><span data-stu-id="083d9-135">MinValue</span></span><br/>     | <span data-ttu-id="083d9-136">entier</span><span class="sxs-lookup"><span data-stu-id="083d9-136">integer</span></span><br/> | <span data-ttu-id="083d9-137">non défini</span><span class="sxs-lookup"><span data-stu-id="083d9-137">undefined</span></span><br/>       |
| <span data-ttu-id="083d9-138">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="083d9-138">Mandatory</span></span><br/>    | <span data-ttu-id="083d9-139">string</span><span class="sxs-lookup"><span data-stu-id="083d9-139">string</span></span><br/>  | <span data-ttu-id="083d9-140">PSK : conditionnel</span><span class="sxs-lookup"><span data-stu-id="083d9-140">psk:Conditional</span></span><br/> |
| <span data-ttu-id="083d9-141">Plusieurs</span><span class="sxs-lookup"><span data-stu-id="083d9-141">Multiple</span></span><br/>     | <span data-ttu-id="083d9-142">integer</span><span class="sxs-lookup"><span data-stu-id="083d9-142">integer</span></span><br/> | <span data-ttu-id="083d9-143">1</span><span class="sxs-lookup"><span data-stu-id="083d9-143">1</span></span><br/>               |
| <span data-ttu-id="083d9-144">Unité</span><span class="sxs-lookup"><span data-stu-id="083d9-144">UnitType</span></span><br/>     | <span data-ttu-id="083d9-145">string</span><span class="sxs-lookup"><span data-stu-id="083d9-145">string</span></span><br/>  | <span data-ttu-id="083d9-146">microns</span><span class="sxs-lookup"><span data-stu-id="083d9-146">microns</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="083d9-147">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="083d9-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="083d9-148">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="083d9-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




