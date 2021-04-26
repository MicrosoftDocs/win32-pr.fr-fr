---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: e1bea06b-11b9-4652-915a-deb563ad59f8
title: PageWatermarkOriginWidth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa78cf29952258a7c6c3489d40291ba8cd4b756c
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996066"
---
# <a name="pagewatermarkoriginwidth"></a><span data-ttu-id="ee0df-104">PageWatermarkOriginWidth</span><span class="sxs-lookup"><span data-stu-id="ee0df-104">PageWatermarkOriginWidth</span></span>

<span data-ttu-id="ee0df-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="ee0df-105">This topic is not current.</span></span> <span data-ttu-id="ee0df-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="ee0df-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="ee0df-107">Spécifie l’origine d’un filigrane par rapport à l’origine du PageImageableSize.</span><span class="sxs-lookup"><span data-stu-id="ee0df-107">Specifies the origin of a watermark relative to the origin of the PageImageableSize.</span></span>

-   [<span data-ttu-id="ee0df-108">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="ee0df-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="ee0df-109">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="ee0df-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="ee0df-110">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="ee0df-110">Element Information</span></span>



| <span data-ttu-id="ee0df-111">Nom</span><span class="sxs-lookup"><span data-stu-id="ee0df-111">Name</span></span> | <span data-ttu-id="ee0df-112">Value</span><span class="sxs-lookup"><span data-stu-id="ee0df-112">Value</span></span> |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="ee0df-113">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="ee0df-113">Element Type</span></span> <br/>   | <span data-ttu-id="ee0df-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="ee0df-114">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="ee0df-115">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="ee0df-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="ee0df-116">Page</span><span class="sxs-lookup"><span data-stu-id="ee0df-116">Page</span></span><br/>                            |
| <span data-ttu-id="ee0df-117">Notes</span><span class="sxs-lookup"><span data-stu-id="ee0df-117">Notes</span></span> <br/>          | <span data-ttu-id="ee0df-118">Lié à l’élément PageWatermark</span><span class="sxs-lookup"><span data-stu-id="ee0df-118">Linked to PageWatermark element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="ee0df-119">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="ee0df-119">Structure Content</span></span>

<span data-ttu-id="ee0df-120">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="ee0df-120">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageWatermarkOriginWidth">
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
    <psf:Value xsi:type="xs:integer">0</psf:Value>
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

## <a name="structure-properties"></a><span data-ttu-id="ee0df-121">Propriétés de structure</span><span class="sxs-lookup"><span data-stu-id="ee0df-121">Structure Properties</span></span>

<span data-ttu-id="ee0df-122">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="ee0df-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="ee0df-123">Propriété</span><span class="sxs-lookup"><span data-stu-id="ee0df-123">Property</span></span>                | <span data-ttu-id="ee0df-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="ee0df-124">xsi:type</span></span>           | <span data-ttu-id="ee0df-125">Value</span><span class="sxs-lookup"><span data-stu-id="ee0df-125">Value</span></span>                                                                  |
|-------------------------|--------------------|------------------------------------------------------------------------|
| <span data-ttu-id="ee0df-126">DataType</span><span class="sxs-lookup"><span data-stu-id="ee0df-126">DataType</span></span><br/>     | <span data-ttu-id="ee0df-127">string</span><span class="sxs-lookup"><span data-stu-id="ee0df-127">string</span></span><br/>  | <span data-ttu-id="ee0df-128">xs:integer</span><span class="sxs-lookup"><span data-stu-id="ee0df-128">xs:integer</span></span><br/>                                                  |
| <span data-ttu-id="ee0df-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="ee0df-129">DefaultValue</span></span><br/> | <span data-ttu-id="ee0df-130">entier</span><span class="sxs-lookup"><span data-stu-id="ee0df-130">integer</span></span><br/> | <span data-ttu-id="ee0df-131">non défini</span><span class="sxs-lookup"><span data-stu-id="ee0df-131">undefined</span></span><br/>                                                   |
| <span data-ttu-id="ee0df-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="ee0df-132">MaxValue</span></span><br/>     | <span data-ttu-id="ee0df-133">entier</span><span class="sxs-lookup"><span data-stu-id="ee0df-133">integer</span></span><br/> | <span data-ttu-id="ee0df-134">Valeur inférieure ou égale à PageImageableSize-ExtentWidth</span><span class="sxs-lookup"><span data-stu-id="ee0df-134">Less than or equal to PageImageableSize - ExtentWidth value</span></span><br/> |
| <span data-ttu-id="ee0df-135">MinValue</span><span class="sxs-lookup"><span data-stu-id="ee0df-135">MinValue</span></span><br/>     | <span data-ttu-id="ee0df-136">entier</span><span class="sxs-lookup"><span data-stu-id="ee0df-136">integer</span></span><br/> | <span data-ttu-id="ee0df-137">0</span><span class="sxs-lookup"><span data-stu-id="ee0df-137">0</span></span><br/>                                                           |
| <span data-ttu-id="ee0df-138">Plusieurs</span><span class="sxs-lookup"><span data-stu-id="ee0df-138">Multiple</span></span><br/>     | <span data-ttu-id="ee0df-139">integer</span><span class="sxs-lookup"><span data-stu-id="ee0df-139">integer</span></span><br/> | <span data-ttu-id="ee0df-140">1</span><span class="sxs-lookup"><span data-stu-id="ee0df-140">1</span></span><br/>                                                           |
| <span data-ttu-id="ee0df-141">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="ee0df-141">Mandatory</span></span><br/>    | <span data-ttu-id="ee0df-142">string</span><span class="sxs-lookup"><span data-stu-id="ee0df-142">string</span></span><br/>  | <span data-ttu-id="ee0df-143">PSK : conditionnel</span><span class="sxs-lookup"><span data-stu-id="ee0df-143">psk:Conditional</span></span><br/>                                             |
| <span data-ttu-id="ee0df-144">Unité</span><span class="sxs-lookup"><span data-stu-id="ee0df-144">UnitType</span></span><br/>     | <span data-ttu-id="ee0df-145">string</span><span class="sxs-lookup"><span data-stu-id="ee0df-145">string</span></span><br/>  | <span data-ttu-id="ee0df-146">microns</span><span class="sxs-lookup"><span data-stu-id="ee0df-146">microns</span></span><br/>                                                     |



 

## <a name="related-topics"></a><span data-ttu-id="ee0df-147">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ee0df-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ee0df-148">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="ee0df-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




