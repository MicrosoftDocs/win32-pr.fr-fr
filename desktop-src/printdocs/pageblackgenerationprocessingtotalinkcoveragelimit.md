---
description: Cette rubrique n’est pas à jour. Pour obtenir les informations les plus récentes, consultez la spécification du schéma d’impression.
ms.assetid: 7ccd02c2-7cec-4d9d-83c1-512f25f4045c
title: PageBlackGenerationProcessingTotalInkCoverageLimit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07566926c2115855ea7321af90e7d1caebcd0a82
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/05/2021
ms.locfileid: "106538446"
---
# <a name="pageblackgenerationprocessingtotalinkcoveragelimit"></a><span data-ttu-id="d31b7-104">PageBlackGenerationProcessingTotalInkCoverageLimit</span><span class="sxs-lookup"><span data-stu-id="d31b7-104">PageBlackGenerationProcessingTotalInkCoverageLimit</span></span>

<span data-ttu-id="d31b7-105">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="d31b7-105">This topic is not current.</span></span> <span data-ttu-id="d31b7-106">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="d31b7-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="d31b7-107">Spécifie la somme maximale autorisée des quatre couvertures d’encre n’importe où dans une image.</span><span class="sxs-lookup"><span data-stu-id="d31b7-107">Specifies the maximum allowed sum of the four ink coverage anywhere in an image.</span></span>

-   [<span data-ttu-id="d31b7-108">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="d31b7-108">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="d31b7-109">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="d31b7-109">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="d31b7-110">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="d31b7-110">Element Information</span></span>



| <span data-ttu-id="d31b7-111">Nom</span><span class="sxs-lookup"><span data-stu-id="d31b7-111">Name</span></span>                       |                                                            |
|----------------------------|------------------------------------------------------------|
| <span data-ttu-id="d31b7-112">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="d31b7-112">Element Type</span></span> <br/>   | <span data-ttu-id="d31b7-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="d31b7-113">ParameterDef</span></span><br/>                                    |
| <span data-ttu-id="d31b7-114">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="d31b7-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="d31b7-115">Page</span><span class="sxs-lookup"><span data-stu-id="d31b7-115">Page</span></span><br/>                                            |
| <span data-ttu-id="d31b7-116">Notes</span><span class="sxs-lookup"><span data-stu-id="d31b7-116">Notes</span></span> <br/>          | <span data-ttu-id="d31b7-117">Lié à l’élément PageBlackGenerationProcessing</span><span class="sxs-lookup"><span data-stu-id="d31b7-117">Linked to PageBlackGenerationProcessing element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="d31b7-118">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="d31b7-118">Structure Content</span></span>

<span data-ttu-id="d31b7-119">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="d31b7-119">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="d31b7-120">Propriétés de structure</span><span class="sxs-lookup"><span data-stu-id="d31b7-120">Structure Properties</span></span>

<span data-ttu-id="d31b7-121">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="d31b7-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="d31b7-122">Propriété</span><span class="sxs-lookup"><span data-stu-id="d31b7-122">Property</span></span>                | <span data-ttu-id="d31b7-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="d31b7-123">xsi:type</span></span>           | <span data-ttu-id="d31b7-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="d31b7-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="d31b7-125">DataType</span><span class="sxs-lookup"><span data-stu-id="d31b7-125">DataType</span></span><br/>     | <span data-ttu-id="d31b7-126">string</span><span class="sxs-lookup"><span data-stu-id="d31b7-126">string</span></span><br/>  | <span data-ttu-id="d31b7-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="d31b7-127">xs:integer</span></span><br/>      |
| <span data-ttu-id="d31b7-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="d31b7-128">DefaultValue</span></span><br/> | <span data-ttu-id="d31b7-129">string</span><span class="sxs-lookup"><span data-stu-id="d31b7-129">string</span></span><br/>  | <span data-ttu-id="d31b7-130">non défini</span><span class="sxs-lookup"><span data-stu-id="d31b7-130">undefined</span></span><br/>       |
| <span data-ttu-id="d31b7-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="d31b7-131">MaxValue</span></span><br/>     | <span data-ttu-id="d31b7-132">entier</span><span class="sxs-lookup"><span data-stu-id="d31b7-132">integer</span></span><br/> | <span data-ttu-id="d31b7-133">400</span><span class="sxs-lookup"><span data-stu-id="d31b7-133">400</span></span><br/>             |
| <span data-ttu-id="d31b7-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="d31b7-134">MinValue</span></span><br/>     | <span data-ttu-id="d31b7-135">entier</span><span class="sxs-lookup"><span data-stu-id="d31b7-135">integer</span></span><br/> | <span data-ttu-id="d31b7-136">200</span><span class="sxs-lookup"><span data-stu-id="d31b7-136">200</span></span><br/>             |
| <span data-ttu-id="d31b7-137">Multiple</span><span class="sxs-lookup"><span data-stu-id="d31b7-137">Multiple</span></span><br/>     | <span data-ttu-id="d31b7-138">integer</span><span class="sxs-lookup"><span data-stu-id="d31b7-138">integer</span></span><br/> | <span data-ttu-id="d31b7-139">1</span><span class="sxs-lookup"><span data-stu-id="d31b7-139">1</span></span><br/>               |
| <span data-ttu-id="d31b7-140">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="d31b7-140">Mandatory</span></span><br/>    | <span data-ttu-id="d31b7-141">string</span><span class="sxs-lookup"><span data-stu-id="d31b7-141">string</span></span><br/>  | <span data-ttu-id="d31b7-142">PSK : conditionnel</span><span class="sxs-lookup"><span data-stu-id="d31b7-142">psk:Conditional</span></span><br/> |
| <span data-ttu-id="d31b7-143">Unité</span><span class="sxs-lookup"><span data-stu-id="d31b7-143">UnitType</span></span><br/>     | <span data-ttu-id="d31b7-144">string</span><span class="sxs-lookup"><span data-stu-id="d31b7-144">string</span></span><br/>  | <span data-ttu-id="d31b7-145">pour cent</span><span class="sxs-lookup"><span data-stu-id="d31b7-145">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="d31b7-146">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d31b7-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d31b7-147">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="d31b7-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




