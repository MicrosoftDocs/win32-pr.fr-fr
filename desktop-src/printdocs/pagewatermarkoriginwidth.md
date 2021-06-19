---
description: Obtenir des informations sur le paramètre PageWatermarkOriginWidth. Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: e1bea06b-11b9-4652-915a-deb563ad59f8
title: PageWatermarkOriginWidth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bffe6457496972231877af2a51e03bc5109083d0
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396004"
---
# <a name="pagewatermarkoriginwidth"></a><span data-ttu-id="584b2-105">PageWatermarkOriginWidth</span><span class="sxs-lookup"><span data-stu-id="584b2-105">PageWatermarkOriginWidth</span></span>

<span data-ttu-id="584b2-106">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="584b2-106">This topic is not current.</span></span> <span data-ttu-id="584b2-107">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="584b2-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="584b2-108">Spécifie l’origine d’un filigrane par rapport à l’origine du PageImageableSize.</span><span class="sxs-lookup"><span data-stu-id="584b2-108">Specifies the origin of a watermark relative to the origin of the PageImageableSize.</span></span>

-   [<span data-ttu-id="584b2-109">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="584b2-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="584b2-110">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="584b2-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="584b2-111">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="584b2-111">Element Information</span></span>



| <span data-ttu-id="584b2-112">Nom</span><span class="sxs-lookup"><span data-stu-id="584b2-112">Name</span></span> | <span data-ttu-id="584b2-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="584b2-113">Value</span></span> |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="584b2-114">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="584b2-114">Element Type</span></span> <br/>   | <span data-ttu-id="584b2-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="584b2-115">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="584b2-116">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="584b2-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="584b2-117">Page</span><span class="sxs-lookup"><span data-stu-id="584b2-117">Page</span></span><br/>                            |
| <span data-ttu-id="584b2-118">Notes</span><span class="sxs-lookup"><span data-stu-id="584b2-118">Notes</span></span> <br/>          | <span data-ttu-id="584b2-119">Lié à l’élément PageWatermark</span><span class="sxs-lookup"><span data-stu-id="584b2-119">Linked to PageWatermark element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="584b2-120">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="584b2-120">Structure Content</span></span>

<span data-ttu-id="584b2-121">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="584b2-121">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="584b2-122">Propriétés de structure</span><span class="sxs-lookup"><span data-stu-id="584b2-122">Structure Properties</span></span>

<span data-ttu-id="584b2-123">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="584b2-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="584b2-124">Propriété</span><span class="sxs-lookup"><span data-stu-id="584b2-124">Property</span></span>                | <span data-ttu-id="584b2-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="584b2-125">xsi:type</span></span>           | <span data-ttu-id="584b2-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="584b2-126">Value</span></span>                                                                  |
|-------------------------|--------------------|------------------------------------------------------------------------|
| <span data-ttu-id="584b2-127">DataType</span><span class="sxs-lookup"><span data-stu-id="584b2-127">DataType</span></span><br/>     | <span data-ttu-id="584b2-128">string</span><span class="sxs-lookup"><span data-stu-id="584b2-128">string</span></span><br/>  | <span data-ttu-id="584b2-129">xs:integer</span><span class="sxs-lookup"><span data-stu-id="584b2-129">xs:integer</span></span><br/>                                                  |
| <span data-ttu-id="584b2-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="584b2-130">DefaultValue</span></span><br/> | <span data-ttu-id="584b2-131">entier</span><span class="sxs-lookup"><span data-stu-id="584b2-131">integer</span></span><br/> | <span data-ttu-id="584b2-132">non défini</span><span class="sxs-lookup"><span data-stu-id="584b2-132">undefined</span></span><br/>                                                   |
| <span data-ttu-id="584b2-133">MaxValue</span><span class="sxs-lookup"><span data-stu-id="584b2-133">MaxValue</span></span><br/>     | <span data-ttu-id="584b2-134">entier</span><span class="sxs-lookup"><span data-stu-id="584b2-134">integer</span></span><br/> | <span data-ttu-id="584b2-135">Valeur inférieure ou égale à PageImageableSize-ExtentWidth</span><span class="sxs-lookup"><span data-stu-id="584b2-135">Less than or equal to PageImageableSize - ExtentWidth value</span></span><br/> |
| <span data-ttu-id="584b2-136">MinValue</span><span class="sxs-lookup"><span data-stu-id="584b2-136">MinValue</span></span><br/>     | <span data-ttu-id="584b2-137">entier</span><span class="sxs-lookup"><span data-stu-id="584b2-137">integer</span></span><br/> | <span data-ttu-id="584b2-138">0</span><span class="sxs-lookup"><span data-stu-id="584b2-138">0</span></span><br/>                                                           |
| <span data-ttu-id="584b2-139">Multiple</span><span class="sxs-lookup"><span data-stu-id="584b2-139">Multiple</span></span><br/>     | <span data-ttu-id="584b2-140">integer</span><span class="sxs-lookup"><span data-stu-id="584b2-140">integer</span></span><br/> | <span data-ttu-id="584b2-141">1</span><span class="sxs-lookup"><span data-stu-id="584b2-141">1</span></span><br/>                                                           |
| <span data-ttu-id="584b2-142">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="584b2-142">Mandatory</span></span><br/>    | <span data-ttu-id="584b2-143">string</span><span class="sxs-lookup"><span data-stu-id="584b2-143">string</span></span><br/>  | <span data-ttu-id="584b2-144">PSK : conditionnel</span><span class="sxs-lookup"><span data-stu-id="584b2-144">psk:Conditional</span></span><br/>                                             |
| <span data-ttu-id="584b2-145">Unité</span><span class="sxs-lookup"><span data-stu-id="584b2-145">UnitType</span></span><br/>     | <span data-ttu-id="584b2-146">string</span><span class="sxs-lookup"><span data-stu-id="584b2-146">string</span></span><br/>  | <span data-ttu-id="584b2-147">microns</span><span class="sxs-lookup"><span data-stu-id="584b2-147">microns</span></span><br/>                                                     |



 

## <a name="related-topics"></a><span data-ttu-id="584b2-148">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="584b2-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="584b2-149">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="584b2-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




