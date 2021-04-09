---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: e1bea06b-11b9-4652-915a-deb563ad59f8
title: PageWatermarkOriginWidth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6780dd5cc3b90a4f15cb6ada66ab82c4269acd82
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "103869649"
---
# <a name="pagewatermarkoriginwidth"></a><span data-ttu-id="ed457-104">PageWatermarkOriginWidth</span><span class="sxs-lookup"><span data-stu-id="ed457-104">PageWatermarkOriginWidth</span></span>

<span data-ttu-id="ed457-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="ed457-105">This topic is not current.</span></span> <span data-ttu-id="ed457-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="ed457-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="ed457-107">Spécifie l’origine d’un filigrane par rapport à l’origine du PageImageableSize.</span><span class="sxs-lookup"><span data-stu-id="ed457-107">Specifies the origin of a watermark relative to the origin of the PageImageableSize.</span></span>

-   [<span data-ttu-id="ed457-108">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="ed457-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="ed457-109">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="ed457-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="ed457-110">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="ed457-110">Element Information</span></span>



| <span data-ttu-id="ed457-111">Nom</span><span class="sxs-lookup"><span data-stu-id="ed457-111">Name</span></span>                       |                                            |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="ed457-112">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="ed457-112">Element Type</span></span> <br/>   | <span data-ttu-id="ed457-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="ed457-113">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="ed457-114">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="ed457-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="ed457-115">Page</span><span class="sxs-lookup"><span data-stu-id="ed457-115">Page</span></span><br/>                            |
| <span data-ttu-id="ed457-116">Notes</span><span class="sxs-lookup"><span data-stu-id="ed457-116">Notes</span></span> <br/>          | <span data-ttu-id="ed457-117">Lié à l’élément PageWatermark</span><span class="sxs-lookup"><span data-stu-id="ed457-117">Linked to PageWatermark element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="ed457-118">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="ed457-118">Structure Content</span></span>

<span data-ttu-id="ed457-119">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="ed457-119">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="ed457-120">Propriétés de structure</span><span class="sxs-lookup"><span data-stu-id="ed457-120">Structure Properties</span></span>

<span data-ttu-id="ed457-121">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="ed457-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="ed457-122">Propriété</span><span class="sxs-lookup"><span data-stu-id="ed457-122">Property</span></span>                | <span data-ttu-id="ed457-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="ed457-123">xsi:type</span></span>           | <span data-ttu-id="ed457-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="ed457-124">Value</span></span>                                                                  |
|-------------------------|--------------------|------------------------------------------------------------------------|
| <span data-ttu-id="ed457-125">DataType</span><span class="sxs-lookup"><span data-stu-id="ed457-125">DataType</span></span><br/>     | <span data-ttu-id="ed457-126">string</span><span class="sxs-lookup"><span data-stu-id="ed457-126">string</span></span><br/>  | <span data-ttu-id="ed457-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="ed457-127">xs:integer</span></span><br/>                                                  |
| <span data-ttu-id="ed457-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="ed457-128">DefaultValue</span></span><br/> | <span data-ttu-id="ed457-129">entier</span><span class="sxs-lookup"><span data-stu-id="ed457-129">integer</span></span><br/> | <span data-ttu-id="ed457-130">non défini</span><span class="sxs-lookup"><span data-stu-id="ed457-130">undefined</span></span><br/>                                                   |
| <span data-ttu-id="ed457-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="ed457-131">MaxValue</span></span><br/>     | <span data-ttu-id="ed457-132">entier</span><span class="sxs-lookup"><span data-stu-id="ed457-132">integer</span></span><br/> | <span data-ttu-id="ed457-133">Valeur inférieure ou égale à PageImageableSize-ExtentWidth</span><span class="sxs-lookup"><span data-stu-id="ed457-133">Less than or equal to PageImageableSize - ExtentWidth value</span></span><br/> |
| <span data-ttu-id="ed457-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="ed457-134">MinValue</span></span><br/>     | <span data-ttu-id="ed457-135">integer</span><span class="sxs-lookup"><span data-stu-id="ed457-135">integer</span></span><br/> | <span data-ttu-id="ed457-136">0</span><span class="sxs-lookup"><span data-stu-id="ed457-136">0</span></span><br/>                                                           |
| <span data-ttu-id="ed457-137">Multiple</span><span class="sxs-lookup"><span data-stu-id="ed457-137">Multiple</span></span><br/>     | <span data-ttu-id="ed457-138">integer</span><span class="sxs-lookup"><span data-stu-id="ed457-138">integer</span></span><br/> | <span data-ttu-id="ed457-139">1</span><span class="sxs-lookup"><span data-stu-id="ed457-139">1</span></span><br/>                                                           |
| <span data-ttu-id="ed457-140">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="ed457-140">Mandatory</span></span><br/>    | <span data-ttu-id="ed457-141">string</span><span class="sxs-lookup"><span data-stu-id="ed457-141">string</span></span><br/>  | <span data-ttu-id="ed457-142">PSK : conditionnel</span><span class="sxs-lookup"><span data-stu-id="ed457-142">psk:Conditional</span></span><br/>                                             |
| <span data-ttu-id="ed457-143">Unité</span><span class="sxs-lookup"><span data-stu-id="ed457-143">UnitType</span></span><br/>     | <span data-ttu-id="ed457-144">string</span><span class="sxs-lookup"><span data-stu-id="ed457-144">string</span></span><br/>  | <span data-ttu-id="ed457-145">microns</span><span class="sxs-lookup"><span data-stu-id="ed457-145">microns</span></span><br/>                                                     |



 

## <a name="related-topics"></a><span data-ttu-id="ed457-146">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ed457-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ed457-147">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="ed457-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




