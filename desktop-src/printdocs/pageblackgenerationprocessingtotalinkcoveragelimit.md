---
description: En savoir plus sur l’élément PageBlackGenerationProcessingTotalInkCoverageLimit, qui spécifie la somme maximale autorisée des quatre couvertures d’encre n’importe où dans une image.
ms.assetid: 7ccd02c2-7cec-4d9d-83c1-512f25f4045c
title: PageBlackGenerationProcessingTotalInkCoverageLimit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68410cabdfafa5ce82450821e4ae45709ee8d4c9
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408442"
---
# <a name="pageblackgenerationprocessingtotalinkcoveragelimit"></a><span data-ttu-id="e757b-103">PageBlackGenerationProcessingTotalInkCoverageLimit</span><span class="sxs-lookup"><span data-stu-id="e757b-103">PageBlackGenerationProcessingTotalInkCoverageLimit</span></span>

<span data-ttu-id="e757b-104">Cette rubrique n’est pas à jour.</span><span class="sxs-lookup"><span data-stu-id="e757b-104">This topic is not current.</span></span> <span data-ttu-id="e757b-105">Pour obtenir les informations les plus récentes, consultez la [spécification du schéma d’impression](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="e757b-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="e757b-106">Spécifie la somme maximale autorisée des quatre couvertures d’encre n’importe où dans une image.</span><span class="sxs-lookup"><span data-stu-id="e757b-106">Specifies the maximum allowed sum of the four ink coverage anywhere in an image.</span></span>

-   [<span data-ttu-id="e757b-107">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="e757b-107">Element Information</span></span>](#element-information)
-   [<span data-ttu-id="e757b-108">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="e757b-108">Structure Content</span></span>](#structure-content)

## <a name="element-information"></a><span data-ttu-id="e757b-109">Informations sur les éléments</span><span class="sxs-lookup"><span data-stu-id="e757b-109">Element Information</span></span>



| <span data-ttu-id="e757b-110">Nom</span><span class="sxs-lookup"><span data-stu-id="e757b-110">Name</span></span> | <span data-ttu-id="e757b-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="e757b-111">Value</span></span> |
|----------------------------|------------------------------------------------------------|
| <span data-ttu-id="e757b-112">Type d'élément</span><span class="sxs-lookup"><span data-stu-id="e757b-112">Element Type</span></span> <br/>   | <span data-ttu-id="e757b-113">ParameterDef</span><span class="sxs-lookup"><span data-stu-id="e757b-113">ParameterDef</span></span><br/>                                    |
| <span data-ttu-id="e757b-114">Préfixe d’étendue</span><span class="sxs-lookup"><span data-stu-id="e757b-114">Scoping Prefix</span></span> <br/> | <span data-ttu-id="e757b-115">Page</span><span class="sxs-lookup"><span data-stu-id="e757b-115">Page</span></span><br/>                                            |
| <span data-ttu-id="e757b-116">Notes</span><span class="sxs-lookup"><span data-stu-id="e757b-116">Notes</span></span> <br/>          | <span data-ttu-id="e757b-117">Lié à l’élément PageBlackGenerationProcessing</span><span class="sxs-lookup"><span data-stu-id="e757b-117">Linked to PageBlackGenerationProcessing element</span></span><br/> |



 

## <a name="structure-content"></a><span data-ttu-id="e757b-118">Structure de contenu</span><span class="sxs-lookup"><span data-stu-id="e757b-118">Structure Content</span></span>

<span data-ttu-id="e757b-119">La structure XML de cet élément est :</span><span class="sxs-lookup"><span data-stu-id="e757b-119">The XML structure of this element is:</span></span>

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

## <a name="structure-properties"></a><span data-ttu-id="e757b-120">Propriétés de structure</span><span class="sxs-lookup"><span data-stu-id="e757b-120">Structure Properties</span></span>

<span data-ttu-id="e757b-121">Le tableau suivant présente les caractéristiques des variables définies dans la structure XML.</span><span class="sxs-lookup"><span data-stu-id="e757b-121">The following table outlines the characteristics of the variables defined in the XML structure.</span></span>



| <span data-ttu-id="e757b-122">Propriété</span><span class="sxs-lookup"><span data-stu-id="e757b-122">Property</span></span>                | <span data-ttu-id="e757b-123">xsi:type</span><span class="sxs-lookup"><span data-stu-id="e757b-123">xsi:type</span></span>           | <span data-ttu-id="e757b-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="e757b-124">Value</span></span>                      |
|-------------------------|--------------------|----------------------------|
| <span data-ttu-id="e757b-125">DataType</span><span class="sxs-lookup"><span data-stu-id="e757b-125">DataType</span></span><br/>     | <span data-ttu-id="e757b-126">string</span><span class="sxs-lookup"><span data-stu-id="e757b-126">string</span></span><br/>  | <span data-ttu-id="e757b-127">xs:integer</span><span class="sxs-lookup"><span data-stu-id="e757b-127">xs:integer</span></span><br/>      |
| <span data-ttu-id="e757b-128">DefaultValue</span><span class="sxs-lookup"><span data-stu-id="e757b-128">DefaultValue</span></span><br/> | <span data-ttu-id="e757b-129">string</span><span class="sxs-lookup"><span data-stu-id="e757b-129">string</span></span><br/>  | <span data-ttu-id="e757b-130">non défini</span><span class="sxs-lookup"><span data-stu-id="e757b-130">undefined</span></span><br/>       |
| <span data-ttu-id="e757b-131">MaxValue</span><span class="sxs-lookup"><span data-stu-id="e757b-131">MaxValue</span></span><br/>     | <span data-ttu-id="e757b-132">entier</span><span class="sxs-lookup"><span data-stu-id="e757b-132">integer</span></span><br/> | <span data-ttu-id="e757b-133">400</span><span class="sxs-lookup"><span data-stu-id="e757b-133">400</span></span><br/>             |
| <span data-ttu-id="e757b-134">MinValue</span><span class="sxs-lookup"><span data-stu-id="e757b-134">MinValue</span></span><br/>     | <span data-ttu-id="e757b-135">entier</span><span class="sxs-lookup"><span data-stu-id="e757b-135">integer</span></span><br/> | <span data-ttu-id="e757b-136">200</span><span class="sxs-lookup"><span data-stu-id="e757b-136">200</span></span><br/>             |
| <span data-ttu-id="e757b-137">Multiple</span><span class="sxs-lookup"><span data-stu-id="e757b-137">Multiple</span></span><br/>     | <span data-ttu-id="e757b-138">integer</span><span class="sxs-lookup"><span data-stu-id="e757b-138">integer</span></span><br/> | <span data-ttu-id="e757b-139">1</span><span class="sxs-lookup"><span data-stu-id="e757b-139">1</span></span><br/>               |
| <span data-ttu-id="e757b-140">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="e757b-140">Mandatory</span></span><br/>    | <span data-ttu-id="e757b-141">string</span><span class="sxs-lookup"><span data-stu-id="e757b-141">string</span></span><br/>  | <span data-ttu-id="e757b-142">PSK : conditionnel</span><span class="sxs-lookup"><span data-stu-id="e757b-142">psk:Conditional</span></span><br/> |
| <span data-ttu-id="e757b-143">Unité</span><span class="sxs-lookup"><span data-stu-id="e757b-143">UnitType</span></span><br/>     | <span data-ttu-id="e757b-144">string</span><span class="sxs-lookup"><span data-stu-id="e757b-144">string</span></span><br/>  | <span data-ttu-id="e757b-145">pour cent</span><span class="sxs-lookup"><span data-stu-id="e757b-145">percent</span></span><br/>         |



 

## <a name="related-topics"></a><span data-ttu-id="e757b-146">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e757b-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e757b-147">Spécification du schéma d’impression</span><span class="sxs-lookup"><span data-stu-id="e757b-147">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




