---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 7ccd02c2-7cec-4d9d-83c1-512f25f4045c
title: PageBlackGenerationProcessingTotalInkCoverageLimit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29918bfe48d1547a3c61b8d79425b36368f6d249
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107993876"
---
# <a name="pageblackgenerationprocessingtotalinkcoveragelimit"></a><span data-ttu-id="85709-104">PageBlackGenerationProcessingTotalInkCoverageLimit</span><span class="sxs-lookup"><span data-stu-id="85709-104">PageBlackGenerationProcessingTotalInkCoverageLimit</span></span>

<span data-ttu-id="85709-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="85709-105">This topic is not current.</span></span> <span data-ttu-id="85709-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="85709-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="85709-107">Spécifie la somme maximale autorisée des quatre couvertures d’encre n’importe où dans une image.</span><span class="sxs-lookup"><span data-stu-id="85709-107">Specifies the maximum allowed sum of the four ink coverage anywhere in an image.</span></span>

-   [<span data-ttu-id="85709-108">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="85709-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="85709-109">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="85709-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="85709-110">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="85709-110">Element Information</span></span>



| <span data-ttu-id="85709-111">Nom</span><span class="sxs-lookup"><span data-stu-id="85709-111">Name</span></span> | <span data-ttu-id="85709-112">Value</span><span class="sxs-lookup"><span data-stu-id="85709-112">Value</span></span> |
|----------------------------|------------------------------------------------------------|
| <span data-ttu-id="85709-113">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="85709-113">Element Type</span></span> <br/>   | <span data-ttu-id="85709-114">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="85709-114">ParameterDef</span></span><br/>                                    |
| <span data-ttu-id="85709-115">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="85709-115">Scoping Prefix</span></span> <br/> | <span data-ttu-id="85709-116">Page</span><span class="sxs-lookup"><span data-stu-id="85709-116">Page</span></span><br/>                                            |
| <span data-ttu-id="85709-117">Notes</span><span class="sxs-lookup"><span data-stu-id="85709-117">Notes</span></span> <br/>          | <span data-ttu-id="85709-118">Lié à l’élément PageBlackGenerationProcessing</span><span class="sxs-lookup"><span data-stu-id="85709-118">Linked to PageBlackGenerationProcessing element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="85709-119">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="85709-119">Structure Content</span></span>

<span data-ttu-id="85709-120">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="85709-120">The XML structure of this element is:</span></span>

``` syntax
<psf:ParameterDef name="psk:PageBlackGenerationProcessingTotalInkCoverageLimit">
  <psf:Property name="psf:DataType">
    <psf:Value xsi:type="xs:string">xs:integer</psf:Value>
  </psf:Property>
  <psf:Property name="psf:DefaultValue">
    <psf:Value xsi:type="xs:string">_Undefined_</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MaxValue">
    <psf:Value xsi:type="xs:integer">400</psf:Value>
  </psf:Property>
  <psf:Property name="psf:MinValue">
    <psf:Value xsi:type="xs:integer">200</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Multiple">
    <psf:Value xsi:type="xs:integer">1</psf:Value>
  </psf:Property>
  <psf:Property name="psf:Mandatory">
    <psf:Value xsi:type="xs:string">psk:Conditional</psf:Value>
  </psf:Property>
  <psf:Property name="psf:UnitType">
    <psf:Value xsi:type="xs:string">percent</psf:Value>
  </psf:Property>
</psf:ParameterDef>
```

## <a name="structure-properties"></a><span data-ttu-id="85709-121">Propriétés de structure</span><span class="sxs-lookup"><span data-stu-id="85709-121">Structure Properties</span></span>

<span data-ttu-id="85709-122">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="85709-122">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="85709-123">Propriété</span><span class="sxs-lookup"><span data-stu-id="85709-123">Property</span></span>                | <span data-ttu-id="85709-124">xsi:type</span><span class="sxs-lookup"><span data-stu-id="85709-124">xsi:type</span></span>           | <span data-ttu-id="85709-125">Value</span><span class="sxs-lookup"><span data-stu-id="85709-125">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="85709-126">DataType</span><span class="sxs-lookup"><span data-stu-id="85709-126">DataType</span></span><br/>     | <span data-ttu-id="85709-127">string</span><span class="sxs-lookup"><span data-stu-id="85709-127">string</span></span><br/>  | <span data-ttu-id="85709-128">xs:integer</span><span class="sxs-lookup"><span data-stu-id="85709-128">xs:integer</span></span><br/>      |
| <span data-ttu-id="85709-129">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="85709-129">DefaultValue</span></span><br/> | <span data-ttu-id="85709-130">string</span><span class="sxs-lookup"><span data-stu-id="85709-130">string</span></span><br/>  | <span data-ttu-id="85709-131">non défini</span><span class="sxs-lookup"><span data-stu-id="85709-131">undefined</span></span><br/>       |
| <span data-ttu-id="85709-132">MaxValue</span><span class="sxs-lookup"><span data-stu-id="85709-132">MaxValue</span></span><br/>     | <span data-ttu-id="85709-133">entier</span><span class="sxs-lookup"><span data-stu-id="85709-133">integer</span></span><br/> | <span data-ttu-id="85709-134">400</span><span class="sxs-lookup"><span data-stu-id="85709-134">400</span></span><br/>             |
| <span data-ttu-id="85709-135">MinValue</span><span class="sxs-lookup"><span data-stu-id="85709-135">MinValue</span></span><br/>     | <span data-ttu-id="85709-136">entier</span><span class="sxs-lookup"><span data-stu-id="85709-136">integer</span></span><br/> | <span data-ttu-id="85709-137">200</span><span class="sxs-lookup"><span data-stu-id="85709-137">200</span></span><br/>             |
| <span data-ttu-id="85709-138">Plusieurs</span><span class="sxs-lookup"><span data-stu-id="85709-138">Multiple</span></span><br/>     | <span data-ttu-id="85709-139">integer</span><span class="sxs-lookup"><span data-stu-id="85709-139">integer</span></span><br/> | <span data-ttu-id="85709-140">1</span><span class="sxs-lookup"><span data-stu-id="85709-140">1</span></span><br/>               |
| <span data-ttu-id="85709-141">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="85709-141">Mandatory</span></span><br/>    | <span data-ttu-id="85709-142">string</span><span class="sxs-lookup"><span data-stu-id="85709-142">string</span></span><br/>  | <span data-ttu-id="85709-143">PSK : conditionnel</span><span class="sxs-lookup"><span data-stu-id="85709-143">psk:Conditional</span></span><br/> |
| <span data-ttu-id="85709-144">Unité</span><span class="sxs-lookup"><span data-stu-id="85709-144">UnitType</span></span><br/>     | <span data-ttu-id="85709-145">string</span><span class="sxs-lookup"><span data-stu-id="85709-145">string</span></span><br/>  | <span data-ttu-id="85709-146">pour cent</span><span class="sxs-lookup"><span data-stu-id="85709-146">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="85709-147">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="85709-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="85709-148">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="85709-148">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




