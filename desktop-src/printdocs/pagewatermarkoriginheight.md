---
description: Obtenir des informations sur le paramètre PageWatermarkOriginHeight. Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: ef429727-d881-408b-95ce-2acce667654a
title: PageWatermarkOriginHeight
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d59e9336088d44cef1941df03319519ae69af1c3
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395984"
---
# <a name="pagewatermarkoriginheight"></a><span data-ttu-id="0388f-105">PageWatermarkOriginHeight</span><span class="sxs-lookup"><span data-stu-id="0388f-105">PageWatermarkOriginHeight</span></span>

<span data-ttu-id="0388f-106">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="0388f-106">This topic is not current.</span></span> <span data-ttu-id="0388f-107">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="0388f-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="0388f-108">Spécifie l’origine d’un filigrane par rapport à l’origine du PageImageableSize.</span><span class="sxs-lookup"><span data-stu-id="0388f-108">Specifies the origin of a watermark relative to the origin of the PageImageableSize.</span></span>

-   [<span data-ttu-id="0388f-109">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="0388f-109">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="0388f-110">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="0388f-110">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="0388f-111">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="0388f-111">Element Information</span></span>



| <span data-ttu-id="0388f-112">Nom</span><span class="sxs-lookup"><span data-stu-id="0388f-112">Name</span></span> | <span data-ttu-id="0388f-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="0388f-113">Value</span></span> |
|----------------------------|--------------------------------------------|
| <span data-ttu-id="0388f-114">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="0388f-114">Element Type</span></span> <br/>   | <span data-ttu-id="0388f-115">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="0388f-115">ParameterDef</span></span><br/>                    |
| <span data-ttu-id="0388f-116">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="0388f-116">Scoping Prefix</span></span> <br/> | <span data-ttu-id="0388f-117">Page</span><span class="sxs-lookup"><span data-stu-id="0388f-117">Page</span></span><br/>                            |
| <span data-ttu-id="0388f-118">Notes</span><span class="sxs-lookup"><span data-stu-id="0388f-118">Notes</span></span> <br/>          | <span data-ttu-id="0388f-119">Lié à l’élément PageWatermark</span><span class="sxs-lookup"><span data-stu-id="0388f-119">Linked to PageWatermark element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="0388f-120">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="0388f-120">Structure Content</span></span>

<span data-ttu-id="0388f-121">La structure XML de cet élément est la suivante :</span><span class="sxs-lookup"><span data-stu-id="0388f-121">The XML structure of this element is as follows:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageWatermarkOriginHeight">
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

## <a name="structure-properties"></a><span data-ttu-id="0388f-122">Propriétés de structure</span><span class="sxs-lookup"><span data-stu-id="0388f-122">Structure Properties</span></span>

<span data-ttu-id="0388f-123">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="0388f-123">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="0388f-124">Propriété</span><span class="sxs-lookup"><span data-stu-id="0388f-124">Property</span></span>                | <span data-ttu-id="0388f-125">xsi:type</span><span class="sxs-lookup"><span data-stu-id="0388f-125">xsi:type</span></span>           | <span data-ttu-id="0388f-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="0388f-126">Value</span></span>                                                                   |
|-------------------------|--------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="0388f-127">DataType</span><span class="sxs-lookup"><span data-stu-id="0388f-127">DataType</span></span><br/>     | <span data-ttu-id="0388f-128">string</span><span class="sxs-lookup"><span data-stu-id="0388f-128">string</span></span><br/>  | <span data-ttu-id="0388f-129">xs:integer</span><span class="sxs-lookup"><span data-stu-id="0388f-129">xs:integer</span></span><br/>                                                   |
| <span data-ttu-id="0388f-130">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="0388f-130">DefaultValue</span></span><br/> | <span data-ttu-id="0388f-131">entier</span><span class="sxs-lookup"><span data-stu-id="0388f-131">integer</span></span><br/> | <span data-ttu-id="0388f-132">non défini</span><span class="sxs-lookup"><span data-stu-id="0388f-132">undefined</span></span><br/>                                                    |
| <span data-ttu-id="0388f-133">MaxValue</span><span class="sxs-lookup"><span data-stu-id="0388f-133">MaxValue</span></span><br/>     | <span data-ttu-id="0388f-134">entier</span><span class="sxs-lookup"><span data-stu-id="0388f-134">integer</span></span><br/> | <span data-ttu-id="0388f-135">Valeur inférieure ou égale à PageImageableSize-ExtentHeight</span><span class="sxs-lookup"><span data-stu-id="0388f-135">Less than or equal to PageImageableSize - ExtentHeight value</span></span><br/> |
| <span data-ttu-id="0388f-136">MinValue</span><span class="sxs-lookup"><span data-stu-id="0388f-136">MinValue</span></span><br/>     | <span data-ttu-id="0388f-137">entier</span><span class="sxs-lookup"><span data-stu-id="0388f-137">integer</span></span><br/> | <span data-ttu-id="0388f-138">0</span><span class="sxs-lookup"><span data-stu-id="0388f-138">0</span></span><br/>                                                            |
| <span data-ttu-id="0388f-139">Multiple</span><span class="sxs-lookup"><span data-stu-id="0388f-139">Multiple</span></span><br/>     | <span data-ttu-id="0388f-140">integer</span><span class="sxs-lookup"><span data-stu-id="0388f-140">integer</span></span><br/> | <span data-ttu-id="0388f-141">1</span><span class="sxs-lookup"><span data-stu-id="0388f-141">1</span></span><br/>                                                            |
| <span data-ttu-id="0388f-142">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="0388f-142">Mandatory</span></span><br/>    | <span data-ttu-id="0388f-143">string</span><span class="sxs-lookup"><span data-stu-id="0388f-143">string</span></span><br/>  | <span data-ttu-id="0388f-144">PSK : conditionnel</span><span class="sxs-lookup"><span data-stu-id="0388f-144">psk:Conditional</span></span><br/>                                              |
| <span data-ttu-id="0388f-145">Unité</span><span class="sxs-lookup"><span data-stu-id="0388f-145">UnitType</span></span><br/>     | <span data-ttu-id="0388f-146">string</span><span class="sxs-lookup"><span data-stu-id="0388f-146">string</span></span><br/>  | <span data-ttu-id="0388f-147">microns</span><span class="sxs-lookup"><span data-stu-id="0388f-147">microns</span></span><br/>                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="0388f-148">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0388f-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0388f-149">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="0388f-149">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




